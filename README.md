# Wild Workouts

## ディレクトリ構造

###  api/openapi

API仕様の定義がここに置かれる。

## openapiのAPI定義ファイルからコードを自動生成するコマンド

`oapi-codegen`コマンドは以下のリポジトリからインストールする。

https://github.com/deepmap/oapi-codegen

trainer用のAPI定義ファイルから各コードを自動生成する例
``` shell
# ymlに定義されたcomponents/schemasから型定義のコードを生成する
oapi-codegen -generate types -o internal/trainer/ports/openapi_types.gen.go -package ports api/openapi/trainer.yml
# ymlに定義されたpathsの定義から実装すべきAPIのインターフェースを生成する
oapi-codegen -generate chi-server -o internal/trainer/ports/openapi_api.gen.go -package ports api/openapi/trainer.yml
```
