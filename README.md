@@ -1,4 +1,52 @@
# README
## usersテーブル

|Column|Type|Options|
|------|----|-------|
|email|integer|null: false, unique: true|
|password|integer|null: false, unique: true|
|name|integer|null: false|

### Association
- belongs_to :group
- belongs_to :grup_chat

## grupsテーブル

|Column|Type|Options|
|------|----|-------|
|grup_name|integer|null: false, unique: true|
|user_id|integer|null: false, unique: true|

### Association
- belongs_to :user
- belongs_to :grup
- belongs_to :grup_chat


## grup_chatテーブル

|Column|Type|Options|
|------|----|-------|
|image|integer|null: false|
|text|integer|null: false|
|user_id|integer|null: false, unique: true|

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