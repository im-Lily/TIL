- mongoDB

  - cmd : mongod --dbpath c\mongo\data\db

  - 입력

    - ``` sql
      insert into table values(value,value)
      ```

    - db.collection_name.insertOne({key : value, key : value}) : 

    - db.collection_name.insertMany([{key : value, key : value}, {key : value, key : value}])

  - 검색

    - db.user.find({condition}, {column list}).limit(5)
    - db.user.find() - select * from user
    - db.user.find({where절},{user_id:1, _id:0}) - select user_id from user
    - db.user.find({gender : 'm'}, {}) - select * from user where xxx
    - db.user.find({user_id : 'eun', gender : 'm'}, {}) - select * from where user_id = xxx and gender = xxxx
    - db.user.find({$or : [{user_id : 'eun'}, {gender : 'm'}]}, {}) - select * from where user_id = xxx or gender = xxxx
      - $or
      - $eq = 
      - $gt >
      - $gte >=
      - $in
      - $t
      - $lte
      - $ne

  - 수정

    - ```sql
      update table
      set column - value
      where condition ;
      ```

    - db.collection_name.updateOne({where}, {set}) : 하나의 row에 대해서만 적용

    - db.collection_name.updateMany({where}, {set})

    - db.user.updateOne({user_id : 'eun'}, {$set : {gender : 'm'}})

    - ```sql
      update user
      set gender = 'm'
      where user_id = 'eun' ;
      ```

  - 삭제

    - ```sql
      delect from table
      where condition ;
      ```

    - db.collection_name.removeOne({where}) : 

    - db.collection_name.removeMany({})