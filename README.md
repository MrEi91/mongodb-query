# mongodb-query


Collection departement

|   Key   |   Type  |
|---------|---------|
|code     | STRING  |
|name     | STRING  |
|major    | STRING  |


Collection student

|   Key   |   Type  |
|---------|---------|
|code     | STRING  |
|name     | STRING  |
|major    | STRING  |

# MongoDB schema Statement untuk :
1. Membuat DB academic & menampilkannya
        QUERY : USE academic, SHOW academic
2. Membuat Collection departement dan student
        QUERY : db.createCollection("departement"), db.createCollection("student")
3. Menampilkan semua Collection & data dalam database
        QUERY : db.collectionsName.find() => (Menampilkan Collection & data dalam DB)
4. Membuat dan mengaktifkan DB
        QUERY : USE databasName => (kalau tidak ada akan membuat DB baru, kalau ada akan mengaktifkan DB yg diselection)
5. Melihat struktur Collection student
        QUERY : var result = db.student.findOne()
                for(var key in result){print (key) ;}
6. Menginputkan 5 data ke dalam Collection departement
        QUERY : db.departement.insert({
            "id": ObjectId("create automatice"),
            "code":'Dev123',
            "name":'IT',
            "major":'DepIT'
          },
          {
            "id": ObjectId("create automatice"),
            "code":'Dev124',
            "name":'Keuangan',
            "major":'DevK'
          }
          {
            "id": ObjectId("create automatice"),
            "code":'Dev125',
            "name":'Humas',
            "major":'DepHumas'
          },
          {
            "id": ObjectId("create automatice"),
            "code":'Dev126',
            "name":'Textil',
            "major":'DepTxt'
          },
          {
            "id": ObjectId("create automatice"),
            "code":'Dev127',
            "name":'ABC',
            "major":'DepABC'
          })
7. Menginputkan 3 data ke dalam collection student beserta reference ke departement
        QUERY : db.student.insert({
          "id": ObjectId("create automatice"),
          "studentId" : '1',
          "name":'name one',
          "address":'Jl. A',
          "departement_ids":[
            ObjectId("get id departement")
          ]
        },
        {
          "id": ObjectId("create automatice"),
          "studentId" : '2',
          "name":'name two',
          "address":'Jl. B',
          departement_ids:[
            ObjectId("get id departement")
          ]
        },
        {
          "id": ObjectId("create automatice"),
          "studentId" : '3',
          "name":'name Three',
          "address":'Jl. C',
          "departement_ids":[
            ObjectId("get id departement")
          ]
        })
8. Melihat isi collection student
        QUERY : db.getCollection('student').find({})
