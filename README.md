## usersテーブル

|Column|Type|Options|
|------|----|-------|
|email|integer|null: false, unique: true|
|password|integer|null: false, unique: true|
|name|integer|null: false|

### Association
- has_many :messages
- has_many :groups_users
- has_many :groups, through: :groups_users


## grupsテーブル

|Column|Type|Options|
|------|----|-------|
|name|integer|null: false, unique: true|

### Association
- has_many :grup_users
- has_many :messages
- has_many :users, through: :groups_users

## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|image|integer|
|text|integer|
|user_id|integer|null: false, unique: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :user
- belongs_to :grup

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user
