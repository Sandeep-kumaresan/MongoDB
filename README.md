# **MongoDB Shell Commands**
This Repository contains basic commands of MongoDB Shell.

# Create
- _show dbs_ --> Shows available DBs.
- _use dbname_ --> To use Database/creates DB if not available.
- _db.collectionname.insertOne({ })_ --> To insert a single record.
- _db.collectionname.insertMany([{ }])_ --> To insert many records.


# Read
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
- _db.collectionname.find({age:{not:{$lte: 21}}})_ --> To find ages not less than equals 21
- _db.collectionname.find({name:{$in: ["Abhishek","Vishwa"]}})_ --> To find records with following names
- _db.collectionname.find({name:{$nin: ["Abhishek","Vishwa"]}})_ --> To find records not in following names
- _db.collectionname.find({age:{$exists: true}})_ --> To find records with age existing
- _db.collectionname.find({age:{$gte:20,$lte:30},name:"Abhishek"})_ --> To find records with age greater than 20 less than 30 and name is Abhishek.

- _db.collectionname.find({$and:[{age:21},{name:"Abhishek"}]})_ --> To find records with both parameters satisfied.
- _db.collectionname.find({$or:[{age:21},{name:"Abhishek"}]})_ --> To find records with any one parameter satisfied.
- _db.collectionname.find({$expr:{$gt:["debit","balance"]}})_ --> To compare and find records within given parameters
- _db.collectionname.findOne({$expr:{$gt:["debit","balance"]}})_ --> To compare and find one record within given parameters
- _db.collectionname.find({"address.city":"Coimbatore"})_ --> To find records of the city in address containing "Coimbatore"
- _db.collectionname.countDocuments({$expr:{$gt:["debit","balance"]}})_ --> To find the count of records within given parameters


# Update
- _db.collectionname.updateOne({age:22},{$set: {age:31}})_ --> To update the record of age containing 22 to 31




