# MVC

Model-View-Controller  
処理の流れは Controller (Input) -> Model (Logic) -> View (Output)

## Controller
入力の変換。

### 役割
- 入力値の不正チェック（ビジネスロジック以外）
- 入力オブジェクトへ変換
- モデルの呼び出し

### サンプルコード
```php
class GachaController extends Controller {
  public function draw() {
    $input = new GachaDrawInputData($_POST['gacha_id'], $_POST['number']);
    $gachaModel->draw($input);
  }
}
```

## Model
ビジネス（ゲーム）ロジック。

## View
画面へ表示。
