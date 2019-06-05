## users table
|column|type|options|
|------|----|-------|
|name     |string  |null: false,unique: true |
|email    |string  |null: false,unique: true |
|password |string  |null: false,unique: true |
|group_id |integer |null: false,unique: true |
|user_id  |integer  |null: false,unique: true |

### Association
- has_many :group through: members
