# 概要

このリポジトリは、PHPとApache、PostgreSQLを使用したWebアプリケーションの開発環境を提供するためのDevContainerです。Visual Studio CodeとDockerを使用して、開発環境を簡単に構築することができます。

## 必要なもの

- Docker
- Visual Studio Code
- Visual Studio CodeのRemote - Containers拡張機能

## 使用方法

1. このリポジトリをクローンします。

2. Visual Studio Codeを開き、コマンドパレットを開きます。 (`Ctrl+Shift+P` on Windows/Linux, `Cmd+Shift+P` on macOS)

3. `Remote-Containers: Open Folder in Container`を選択し、先ほどクローンしたリポジトリのディレクトリを選択します。

4. DevContainerが起動するのを待ちます。初回の起動時には、Dockerイメージのビルドや必要なライブラリのダウンロードなどが行われるため、起動には数分かかる場合があります。

5. Visual Studio Codeのターミナルから、ApacheとPostgreSQLを起動します。

6. ブラウザから`http://localhost`にアクセスし、Webアプリケーションが正しく表示されることを確認します。

## DevContainerの構成

このDevContainerは、以下の構成で構成されています。

- `mcr.microsoft.com/devcontainers/universal:2`をベースとしたDockerイメージ
- PHP 7.4、PHP 8.1の開発環境をインストールするための`ghcr.io/devcontainers/features/php:1`機能
- Apache Webサーバーの設定
- PostgreSQLデータベースサーバーの設定

## カスタマイズ

このDevContainerをカスタマイズするには、`.devcontainer/devcontainer.json`ファイルを編集します。必要に応じて、Dockerイメージ、開発環境、Webサーバーやデータベースの設定を変更することができます。

また、DockerfileやApacheの設定ファイルなどを変更することで、よりカスタマイズされたDevContainerを作成することもできます。詳細については、[Visual Studio Codeのドキュメント](https://code.visualstudio.com/docs/remote/create-dev-container)を参照してください。


