# 概要
# プロジェクト構成

### ColorUnityProject
 -  アプリ制作を行うUnityプロジェクト
### Packages
 - アプリに依存しないパッケージの格納先

# コーディングガイドライン
### 概要
- 基本、"UpperCamelCase" (="PascalCase"),"camelCase"を使用する。
- "snake_case", "UPPER_SNAKE_CASE"は使用しない。
- "m_", "s_", "_"のようなプリフィックスは使わない。
- ローカル変数は"var"を使う
- 定数はstatic readonlyを使って定義する（constは使わない）
- namespaceは、フォルダ構成に合わせて命名する。ただし、"Scripts"は省略する。"Runtime","Editor"などは任意。
  - 例) App.Sample

### サンプル
```C#
namespace App.Sample
{
    class MyClass : MonoBehaviour
    {
        public static readonly int Constant = 100;
        [SerializeField] private int value = 1;
        private string name = "";

        public int Property { get; set; }
        public int Value => value;
        public string Name => name;

        void Start() { }
        void Update() { }

        public void Method()
        {
            var localVariable = 1;

            void LocalFunc()
            {

            }
        }

        private void PrivateMethod()
    }
}
```

### "UpperCamelCase"に該当するもの
- ファイル
- namespace
- クラス
- enum
- 定数
- public メンバ変数
- プロパティ
- 関数
- 構造体

### "lowerCamelCase"に該当するもの
- ローカル変数
- シリアライズフィールド
- 引数
- private メンバ変数

# プロジェクトに追加した外部パッケージを記載
|名前   |ライセンス |Version    |リンク |
|:------|---------:|:---------:|:-----:|
|UniTask|MIT|2.5.10|https://github.com/Cysharp/UniTask|
|R3|MIT|1.2.9|https://github.com/Cysharp/R3|
|MessagePipe|MIT|1.8.1|https://github.com/Cysharp/MessagePipe|
|ZString|MIT|2.6.0|https://github.com/Cysharp/ZString|
|VContainer|MIT|1.16.5|https://vcontainer.hadashikick.jp/ja/|

