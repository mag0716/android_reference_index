# Android Sunflower

* https://github.com/googlesamples/android-sunflower

## 概要

Jetpack を使ったベストプラクティス
一覧に表示された植物をお気に入りとして保存できる

## 対象

https://github.com/googlesamples/android-sunflower/commit/ee23fbc7608ea99a6fdd008885f0ae09d842dd47

## 全体設計

* InjecorUtils
  * Repository, ViewModelFactory を Inject するためのクラス
  * interface などは定義していない

## Navigation

* GardenActivity, PlantDetailActivity があるが利用されているのは、GardenActivity
* GrardenActivity
  * nav_graph のみ
    * Destination は GardenFragment, PlantListFragment のみ
    * startDestination は GardenFragment
    * Action はなし
  * NavigationDrawer のみ連携している
  * ActionBarDrawerToggle は自前でハンドリングしている
    * [疑問点] 不要なはずだが、なぜ？
* PlantDetailActivity
  * PlantDetailActivity への遷移は、PlantAdapter 内で行なっている
  * PlantDetailActivity から戻る場合は、navigateUpTo を利用しているので、GardenFragment が必ず表示される
  * PlantDetailFragment は自前で add している

## Room

* AppDatabase
  * インスタンス生成時に synchronized を使っている
* Plant
  * デフォルトで保存されている植物
  * PlantRepository
    * インスタンスに `@Volatile` を指定している
* GardenPlanting
  * ユーザーが保存した植物
  * `foreignKeys`
  * GardenPlantingDao
    * LiveData を返却
    * Plant と GardenPlanting のマッピング時に `@Transaction` を利用している
* PlantAndGardenPlantings
  * `@Embedded`, `@Relation`
* Converter
  * Calendar <-> Long

## ViewModel

* `ViewModelProvider.of` を通じて取得している

## LiveData

* PlantListFragment
  * subscribeUi
    * onCreateView で呼び出している

## WorkManager

* SeedDatabaseWorker
  * AppDatabase で利用している
    * Constraints などは指定なし
  * DB 新規作成時に、assets から読み出して、DB に insert している

## Test
