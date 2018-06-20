# android_reference_index

Android 開発で役に立つ情報を集約する

## 開発環境

### Android Studio

* https://developer.android.com/studio/index.html
* https://developer.android.com/studio/preview/index.html
* [Android Studio Release Notes](https://developer.android.com/studio/releases/index.html)
* [Android Plugin for Gradle Release Notes](https://developer.android.com/studio/releases/gradle-plugin.html)

### Jetpack

* [Jetpackを使ったベストプラクティス](https://github.com/googlesamples/android-sunflower)

### Kotlin

* [Cheat Sheet](https://blog.kotlin-academy.com/kotlin-cheat-sheet-1137588c75a)

#### coroutines

* https://github.com/pljp/kotlinx.coroutines/blob/japanese_translation/coroutines-guide.md
* [Android Coroutine Recipes](https://proandroiddev.com/android-coroutine-recipes-33467a4302e9)

#### Lint

* https://medium.com/@takusemba/make-your-code-clean-with-ktlint-bf651c5924e8
    * ktlint にカスタムルールを追加する

### support library など

#### Data Binding

* https://github.com/googlesamples/android-databinding

### ライブラリ

#### Parceler

* [android-state](https://github.com/evernote/android-state)
    * IcePick をベースとしたライブラリ
        * Kotlin のクラスに対応していない IcePick の欠点を補うライブラリ
        * IceKick というライブラリもあるが、Java と Kotlin が共存している時に2つのライブラリを使う必要がある

## 設計

## Fragment

* http://nein37.hatenablog.com/entry/2018/05/06/204943
   * setPrimaryNavigationFragment 知らなかった

## UI

### Material Design

* [Material Design](https://material.io/design/)

### RecyclerView

* https://github.com/andyb129/ZigzagRecyclerView
    * 実装未確認
    * 1行に画像を2つずつ配置し、ジグザクな線で区切るライブラリ
    * 区切り線はジャギーが目立つ

### Pinterest みたいなアスペクト比が異なる画像を表示する UI

* [Aspect Ratio in Staggered LayoutManager using Constraint Layout](https://medium.com/@burhanrashid52/aspect-ratio-in-staggered-layoutmanager-using-constraint-layout-9845d04d1962)
   * API で画像のサイズを取得して、ConstraintSet で適用している

### ViewPager

* [https://medium.com/inloopx/adventures-with-fragmentstatepageradapter-4f56a643f8e0](https://medium.com/inloopx/adventures-with-fragmentstatepageradapter-4f56a643f8e0)
    * FragmentPageStateAdapter よりも PageAdapter を継承したクラスを作った方がいい

## 機能

### 音楽プレイヤー

* [イマドキなAndroid音楽プレーヤーの作り方](https://qiita.com/siy1121/items/f01167186a6677c22435)

### ExoPlayer

* [Building a video player app in Android (Part 1 / 5)](https://medium.com/google-developers/building-a-video-player-app-in-android-part-1-5-d95770ef762d)

## デザイン

### Material Design

* [Navigation Drawer](./MaterialDesign/NavigationDrawer.md)

## アニメーション

* [Shape Shifter](https://shapeshifter.design/)

## デバッグ

### Activity 再生成時などに余計な Fragment が add されていないかを確認する

`adb shell dumpsys activity top`

### 他のアプリのレイアウトを調べる

* https://speakerdeck.com/operando/dezainfalseshi-zhuang-wojie-ti-suruji-shu

### apk を引っこ抜く

* `adb shell dumpsys activity activities | grep apk | sed -e 's/ *baseDir=//g' | peco | xargs adb pull`
   * https://qiita.com/operandoOS/items/6fa77037560e52d11352

## テスト
