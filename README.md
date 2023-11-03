# Code Museum

このリポジトリは、Code Museum のダウンロード用リポジトリです。  
Code Museum のソースコードを公開するまで、インストーラーのみをこのリポジトリで提供します。

## インストール

インストールは、[Release](https://github.com/waryu-YND/code-museum-release/releases/latest) より、OSにあったインストーラーをダウンロードしてください。

## 設定

> **Warning**
> config.jsonの設定を行わないと、AI機能などが使えません。
> インストール後、設定するようにしてください

設定は、configファイルに記述してください  
configファイルは、  

|OS|Path|
|---|---|
|Windows|`%APPDATA%/code-museum/config.json`|
|MacOS|`$HOME/Library/Application Support/code-museum/config.json`|
|Linux|`$XDG_CONFIG_HOME` or `$HOME/.config/code-museum/config.json`|

に存在します。

```config.json
{
    "executeSelection": {
        "outputFontSize": 14,
        "editor": {
            "fontSize": 14
        }
    },
    "editor": {
        "fontSize": 14
    },
    "askAI": {
        "enableAI": true,
        "model": "gpt-3.5-turbo",
	      "apiKey": "Your API Key"
    }
}
```

configファイルはこのようなものになっています。

### executeSelection/outputFontSize

|Type|
|---|
|number|

範囲実行による出力のフォントサイズを設定します。 

### executeSelection/editor/fontSize

|Type|
|---|
|number|

範囲実行のエディタのフォントサイズを設定します。 

### editor/fontSize

|Type|
|---|
|number|

editorのフォントサイズを設定します。

### askAI/enableAI

|Type|
|---|
|boolean|

AIの機能を利用するかどうかを設定します。

### askAI/model

|Type|
|---|
|string|

GPTの利用するモデルを設定します。  
`gpt-3.5-turbo` をお勧めします。

### askAI/apiKey

|Type|
|---|
|string|

GPTのAPI Keyを設定します。  
`askAI/enableAI` を `true` にしていても、この設定を行わなければ利用できません。


