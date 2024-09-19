#MongoDB Shell Commands
This Repository contains basic commands of MongoDB Shell.
- _show dbs_ --> Shows available DBs.
- _use dbname_ --> To use Database/creates DB if not available.
- _db.collectionname.insertOne({ })_ --> To insert a single record.
- _db.collectionname.insertMany([{ }])_ --> To insert many records.
- _db.collectionname.find()_ --> To get all records.
- _db.collectionname.find(fieldname)_ --> To get particular record .
- _db.collectionname.find().limit(2)_ --> To limit results.
- _db.collectionname.find().sort({name:1,age:-1})_ --> To sort the results, 1 is ascending order, -1 is descending order.
- _db.collectionname.find().skip(2)_  --> To skip 1st 2 values
- _db.collectionname.find({name:"Sandeep"},{name:1,age:0})_ --> To find names matching Sandeep, but shows only Name not Age.
- _db.collectionname.find({name:{$eq: "Vishwa"}})_ --> To find names matching exactly Vishwa
- _db.collectionname.find({name:{$ne: "Vishwa"}})_ --> To find names not equals exactly Vishwa
- _db.collectionname.find({age:{$gt: 21}})_ --> To find ages greater than 21
- _db.collectionname.find({age:{$gte: 21}})_ --> To find ages greater than equals 21
- _db.collectionname.find({age:{$lt: 21}})_ --> To find ages less than 21
- _db.collectionname.find({age:{$lte: 21}})_ --> To find ages less than equals 21
- _db.collectionname.find({name:{$in: ["Abhishek","Vishwa"]}})_ --> To find records with following names
