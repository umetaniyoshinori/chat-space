## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|


### Association
- has_many :groups_users
- has_many :messages
- has_many :users, through: :groups_users

## usersテーブル

|Column|Type|Options|
|------|----|-------|

|name|strig|null: false|
|email|string|null: false|
|password|string|null: false|

### Association
- has_many :groups_users
- has_many :messages
- has_many :groups, through: :groups_users

## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|text|string|
|image|string|null: false|
|user_id|integer|null: false|
|group_id|integer|null: false|

### Association

- belongs_to :user
- belongs_to :group


