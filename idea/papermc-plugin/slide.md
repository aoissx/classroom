---
marp: true
header: "**マイクラプラグインの作り方**"
footer: "by **＠aoissx**"
size: 16:9
---

# マイクラプラグインの作り方

著: 星野あおい

---

## 目次

1. プラグインとは
2. プラグインを作る準備
3. 簡単なプラグインの作り方
4. 少し難しいプラグインの作り方
5. コツ
6. 終わりに

---

## 対象読者

- プラグインを作ろうと思っている人
- プログラミングに触れたことがある人
  - "Hello, world" をしたことがあればよい。

---

## プラグインとは

　プラグインとは、マイクラに元々存在する要素を組み合わせたり、
改造したりするもの。  

MODではない。

---

## MODとの違い

プラグインでは

- 新しい要素を追加することはできない。
- サーバーで動かす必要がある。

MODのように、**新しいモンスター**や**武器**を追加できない。
既存の武器の攻撃力を上げたり、武器を使う時にエフェクトを追加するなどはできる。

また、MODはクライアントのみで動かすことが可能だが、プラグインはマイクラサーバーの中で動かさなければならない。

---

## プラグインを作る準備

今回は**Windows**で作成するものとして説明をします。  
今回インストールするものは下記の2つです。  

- [Scoop](https://scoop.sh/)
- [IntelliJ IDEA](https://www.jetbrains.com/idea/)

Scoopは、Javaやその他開発ツールをインストールする際に使用する。
IntelliJ IDEA (以下 Idea)は、統合開発環境です。実際に開発を行います。  

---

## Scoopのインストール

### Scoopとは

さまざまなツールやソフトをターミナルから
インストールできるパッケージマネージャ。慣れるとマジで便利。

### インストール方法

1. PowerShellを開く
2. 下記のコードをコピーしてPowershellで実行

    ```powershell
    Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
    irm get.scoop.sh | iex
    ```

3. 完了！

---

## Scoopを使ってツールをインストール

- git
- aria2
- openjdk17

上記の3つをインストールします。

```powershell
scoop install git            # Gitのインストール
scoop install aria2          # ダウンロードを高速化するやつ
scoop bucket add java        # Javaをインストールする準備
scoop install java/openjdk17 # Javaをインストールする
```

---

## Ideaをインストール

---
