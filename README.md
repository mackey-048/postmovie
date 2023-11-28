# テーブル設計

## userテーブル

| Column                | Type   | Options                   |
| --------------------- | ------ | ------------------------- |
| nickname              | string | null: false               |
| first_name            | string | null: false               |
| last_name             | string | null: false               |
| email                 | string | null: false, unique: true |
| encrypted_password    | string | null: false               |

## moviesテーブル

| Column                | Type    | Options                        |
| --------------------- | ------- | ------------------------------ |
| title                 | string  | null: false                    |
| text                  | string  |                                |
| movie                 | string  | null: false                    |
| user_id               | integer | null: false, foreign_key: true |

## commentsテーブル

| Column                | Type    | Options                        |
| --------------------- | ------- | ------------------------------ |
| user_id               | integer | null: false, foreign_key: true |
| movie_id              | integer | null: false, foreign_key: true |

## favoritesテーブル

| Column                | Type    | Options                        |
| --------------------- | ------- | ------------------------------ |
| user_id               | integer | null: false, foreign_key: true |
| movie_id              | integer | null: false, foreign_key: true |

## groupsテーブル
| Column                | Type   | Options                        |
| --------------------- | ------ | ------------------------------ |
| name                  | string | null: false                    |
| info                  | text   |                                |

## group_membersテーブル

| Column                | Type    | Options                        |
| --------------------- | ------- | ------------------------------ |
| user_id               | integer | null: false, foreign_key: true |