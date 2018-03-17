# Navigation Drawer

Navigation Drawer は左からスライドして、アプリの遷移先を含むもの

## Content

### Elevation

* Navigation Drawer の高さはステータスバーも含んだデバイスの高さと同じ
* elevation は 16dp
* Navigaition Drawer の後ろのコンテンツは暗くなった状態でみえる

### Selection state

* リストの項目が選択状態になると、その項目の色は primary color か黒に変更される
* タッチ時には ripple effect が走る
* ripple/ハイライトの色のコントラストが十分でない場合は、primary color の darker tint を利用する

### Dividers

* divider の幅は Navigation Drawer の幅と同じ
* 上下のパディングは 8dp

### Scrolling

* Navigation Drawer はスクロール可能

### Settings and support

* 設定やサポートなどは下部に配置する

## Behavior

### Permanent

* Permanent Navigation Drawer は常に左端に固定されて表示される Navigation Drawer
* 右側のコンテンツと同じ elevation
* デスクトップ向けにデフォルトにするのが推奨される

#### Types of permanent navigation drawers

* Full-height navigation drawer
* Navigation drawer clipped under the app bar：Toolbar を隠さない
* Floating navigation drawer

### Persistent

* Persistent Navigation Drawer は開閉がトグルできる
* コンテンツと elevation が同じ
* デフォルトでは閉じていて、メニューアイコンの選択で開き、ユーザが閉じるまで開いたままになる
* Drawer の状態はアクション間、セッション間で記憶されている
* ★Drawer がページグリッドの外側で開いている時、他のコンテンツのサイズを変更し、より小さい viewport に適合させる
* Persistent Navigation Drawer はモバイルよりも大きいサイズの端末で利用可能
* Persistent Navigation Drawer は up ボタンを必要とするような複数階層のアプリには推奨されない

#### Mini variant

* コンテンツと同じ elevation で Toolbar に重ならない形で幅の小さい Drawer が配置される
* 開いた場合は、通常の Persistent Navigation Drawer と同じ
* コンテンツを素早く選択させる必要がアプリに推奨される

### Temporary

* デフォルトは閉じていて、開閉がトグルできる
* 項目を選択するまでコンテンツの上に表示される
* タブレット向けには推奨で、モバイル向けには必須

## reference


* https://material.io/guidelines/patterns/navigation-drawer.html
