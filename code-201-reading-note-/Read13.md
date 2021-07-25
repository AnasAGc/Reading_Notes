# HTML5 STORAGE

 + is a specification named Web Storage some browser call it "Local Storage” or “DOM Storage"  : it’s a way for web pages to store named key/value pairs locally, Like cookies

 + storage data based on named key/value pairs , we store data based on a named key, then you can retrieve that data with the same key

+ Eveythings save in Localstorge is a strain 

 ## How To save data in Localstorge .

 by using setitem ("key","value")

 ``` 
Localstorge.setitem ("me","Anas Abu Ghaliha")

 ```
## How To retrive data in Localstorge
 by using getitem ("key")
```
let user1;

user1= Localstorge.getitem(me );

console.log (user1);
// the result will be Anas Abu Ghaliha
```
 ## How To Save Multidimensional Data In Localstorge .

 1- we need to convert the to a strain by using JSON Strainify

````
 let stu={

     "name":"Anas"
     "age":"23"
 }

 let strainSTU=JSON.strinify(stu)

 Localstorge.setitem("student1","strainSTU")

 ````
## How To Access Multidimensional Data In Localstorge .

 we need to convert it back to the same data it was by uing JSON parse
```
let a1=Localstorge.getitem(student1)
 let obj=Json.parse(a1)

 ```