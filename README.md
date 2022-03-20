# README

## users テーブル

| Column             | Type   | Options                |
| ------------------ | ------ | -----------------------|
| email              | string | null: false, unique key|
| encrypted_password | string | null: false            |
| name               | string | null: false            |
| profile            | text   | null: false            |
| occupation         | text   | null: false            |
| position           | text   | null: false            |

### Association


## prototypes テーブル

| Column     | Type   | Options                       |
| ---------- | ------ | ------------------------------|
| title      | string | null: false                   |
| catch_copy | text   | null: false                   |
| concept    | text   | null: false                   |
| user       | text   | null: false, foreign_key: true|

## comments テーブル

| Column    | Type       | Options                        |
| --------- | ---------- | ------------------------------ |
| content   | references | null: false, foreign_key: true |
| prototype | references | null: false, foreign_key: true |
| user      | references | null: false, foreign_key: true |