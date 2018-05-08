# android_reference_index

Android 開発で役に立つ情報を集約する

## 開発環境

### Android Studio

* https://developer.android.com/studio/index.html
* https://developer.android.com/studio/preview/index.html
* [Android Studio Release Notes](https://developer.android.com/studio/releases/index.html)
* [Android Plugin for Gradle Release Notes](https://developer.android.com/studio/releases/gradle-plugin.html)

### Kotlin

#### coroutines

* https://github.com/pljp/kotlinx.coroutines/blob/japanese_translation/coroutines-guide.md
* [Android Coroutine Recipes](https://proandroiddev.com/android-coroutine-recipes-33467a4302e9)

#### Lint

* https://medium.com/@takusemba/make-your-code-clean-with-ktlint-bf651c5924e8
    * ktlint にカスタムルールを追加する

### support library など

#### Data Binding

* https://github.com/googlesamples/android-databinding

## 設計

## UI

### RecyclerView

* https://github.com/andyb129/ZigzagRecyclerView
    * 実装未確認
    * 1行に画像を2つずつ配置し、ジグザクな線で区切るライブラリ
    * 区切り線はジャギーが目立つ

## 機能

### 音楽プレイヤー

* [イマドキなAndroid音楽プレーヤーの作り方](https://qiita.com/siy1121/items/f01167186a6677c22435)

### ExoPlayer

* [Building a video player app in Android (Part 1 / 5)](https://medium.com/google-developers/building-a-video-player-app-in-android-part-1-5-d95770ef762d)

## デザイン

### Material Design

* [Navigation Drawer](./MaterialDesign/NavigationDrawer.md)

## デバッグ

### Activity 再生成時などに余計な Fragment が add されていないかを確認する

`adb shell dumpsys activity top`

### 他のアプリのレイアウトを調べる

* https://speakerdeck.com/operando/dezainfalseshi-zhuang-wojie-ti-suruji-shu

## テスト
