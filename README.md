# README

This README would normally document whatever steps are necessary to get the
application up and running.

<<<<<<< HEAD
### Association
- belongs_to :group
- belongs_to :user

## groupsテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false,unique: true|


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
|text|text|
|image|string|
|user_id|integer|null: false,foreign_key: true|
|group_id|integer|null: false,foreign_key: true|

### Association

- belongs_to :user
- belongs_to :group


=======
Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
>>>>>>> parent of 835638d... Update README.md
