# README
## usersテーブル

|Column|Type|Options|
|------|----|-------|
|email|integer|null: false, unique: true|
|password|integer|null: false, unique: true|
|name|integer|null: false|

### Association
- has_many :messages 
- has_many :groups_users 



## grupsテーブル

|Column|Type|Options|
|------|----|-------|
|name|integer|null: false, unique: true|
|user_id|integer|null: false, unique: true|

### Association
- has_many :grup_users 
- has_many :messages 


## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|image|integer|
|text|integer|
|user_id|integer|null: false, unique: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :grup

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user



This README would normally document whatever steps are necessary to get the
application up and running.

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
