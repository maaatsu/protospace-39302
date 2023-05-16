# テーブル設計

## users テーブル

| Column             | Type   | Options     | Key |
| ------------------ | ------ | ----------- |     |
| email              | string | null: false | UNI |
| encrypted_password | string | null: false |     |
| name               | string | null: false |     |
| profile            | text   | null: false |     |
| occupation         | text   | null: false |     |
| position           | text   | null: false |     |


## prototypes テーブル

| Column      | Type       | Options                        |
| ----------- | ---------- | ------------------------------ |
| title       | string     | null: false                    |
| catch_copy  | text       | null: false                    |
| concept     | text       | null: false                    |
| user        | references | null: false, foreign_key: true |


## comments テーブル

| Column      | Type       | Options                        |
| ----------- | ---------- | ------------------------------ |
| concept     | text       | null: false                    |
| prototype   | references | null: false, foreign_key: true |
| user        | references | null: false, foreign_key: true |