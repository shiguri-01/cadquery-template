## 必要なもの

- uv
- Git
- GitHub CLI
- VSCode


## セットアップ手順

1. **リポジトリを作成し、VSCodeで開く**

   ターミナルで以下のコマンドを実行する。
   `<name>`の部分は好きな名前に置き換えること。

    ```
    gh repo new <name> --clone --private --template=shiguri-01/cadquery-demo-2
    code <name>
    ```

2. **仮想環境のセットアップとGitフックのインストール**

   VSCodeのターミナルで以下のコマンドを実行する。

    ```
    uv sync
    uv run lefthook install
    ```

3. **Notebookのカーネルを選択**

   1. src/main.ipynbを開く。
   2.  エディタ右上のSelect Kernelボタンをクリックする。
   3. 一覧から、プロジェクト内に作成された仮想環境（さっきの`<name>`と同じ名前）のカーネルを選択する。

4. **推奨のVSCode拡張機能をインストール**

   1. サイドバーのExtensions（拡張機能）タブを開く。
   2. Recomended欄の以下の拡張機能をインストールする。
      - **OCP CAD Viewer**: CadQueryの3DモデルをVSCode上で表示する
      - **Jupyter**: NotebookをVSCodeで編集・実行する

