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
- has_many :chat
- has_many :image

## userテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|name|strig|null: false|
|email|string,integer|
|password|{8,}

### Association
- has_many :groups_users
- has_many :chat
- has_many :image

## chatテーブル

|Column|Type|Options|
|------|----|-------|
|chat_id|integer|null: false, foreign_key: true|


### Association
- belongs_to :image
- belongs_to :user
- belongs_to :group

## imageテーブル

|Column|Type|Options|
|------|----|-------|
|image_id|integer|null: false, foreign_key: true|


### Association
- belongs_to :chat
- belongs_to :user
- belongs_to :group
