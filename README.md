## users table
|column|type|options|
|------|----|-------|
|name     |string  |null: false,unique: true |

### Association
- has_many :groups through: members
- has_many :messages
- has_many :members

## messages table
|column|type|options|
|------|----|-------|
|body    |text   |            |
|image   |string |　　　　　　  |
|user_id    |integer |null: false |
|group_id   |integer |null: false |

### association
- belongs_to :user
- belongs_to :group

## groups table
|column|type|options|
|------|----|-------|
|name|string |null: false |

### association
- has_many :members
- has_many :messages
- has_many :users through: members

## membersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user
