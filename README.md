# CadQueryテンプレート

VSCodeでCadQueryによる3Dモデリングを始めるためのテンプレート

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
    gh repo new <name> --clone --private --template=shiguri-01/cadquery-template
    code <name>
    ```

2. **推奨のVSCode拡張機能をインストール**

   1. サイドバーのExtensions（拡張機能）タブを開く。
   2. Recommended欄の以下の拡張機能をインストールする。
      - **Python**: Pythonの開発環境を提供する
      - **Jupyter**: Notebook形式のファイルを扱えるようにする
      - **OCP CAD Viewer**: CadQueryの3Dモデルのプレビューを表示する
      - **vscode-stl-viewwer**: エクスポートしたSTLファイルのプレビューを表示する
      - **Ruff**: Pythonのリンター・フォーマッター

3. **仮想環境のセットアップとGitフックのインストール**

   VSCodeのターミナルで以下のコマンドを実行する。

    ```
    uv sync
    uv run lefthook install
    ```

4. **Notebookのカーネルを選択**

   1. src/main.ipynbを開く。
   2.  エディタ右上のSelect Kernelボタンをクリックする。
   3. 一覧から、`cadquery-project`を選択する。

5. **OCP CAD Viewerのカーネル設定**

   1. サイドバーの`OCP CAD Viewer`タブを開く。
   2. カーネル選択ボタンをクリックし、`cadquery-project`を選択する。
