# テーブル設計

## users テーブル

| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| name               | string | null: false |
| email              | string | null: false |
| encrypted_password | string | null: false |
| nickname           | string | null: false |

### Association

- has_many :routines
- has_many :routine_introductions


## routines テーブル

| Column         | Type   | Options     |
| ---------------| ------ | ----------- |
| routine_name   | string | null: false |
| reason         | text   | null: false |

### Association

- belongs_to :user

## routine_introductions テーブル

| Column         | Type   | Options     |
| ---------------| ------ | ----------- |
| title          | string | null: false |
| continued_time | siring | null: false |
| introduction   | text   | null: false |
| result         | text   | null: false |

### Association

- belongs_to :user