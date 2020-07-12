## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## groupテーブル

|Column|Type|Options|
|------|----|-------|
|group_name|string|null: false|
|group_id|integer|null: false, foreign_key: true|

### Association
- has_many :groups_users
- has_many :chats


## userテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|name|strig|null: false|
|email|string,integer|
|password|{8,}

### Association
- has_many :groups_users
- has_many :chats


## chatテーブル

|Column|Type|Options|
|------|----|-------|
|chat_id|integer|null: false, foreign_key: true|
|image|integer|null: false, foreign_key: true|

### Association

- belongs_to :user
- belongs_to :group


