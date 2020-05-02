# MVC

Model-View-Controller  
処理の流れは Controller (Input) -> Model (Logic) -> View (Output)

## Controller
入力の変換。

```php
class GachaController extends Controller {
  public function draw() {
    $input = new GachaDrawInputData($_POST);
    $gachaModel->draw($input);
  }
}
```

## Model
ビジネス（ゲーム）ロジック。

## View
画面へ表示。
