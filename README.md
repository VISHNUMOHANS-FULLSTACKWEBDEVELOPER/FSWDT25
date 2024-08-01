# FSWDT25
Day25
<!DOCTYPE html>
<html>
    <head>
        <title>Array Methods & Promises</title>
    </head>
    <body>
        <h1>Array Methods & Promises</h1>
        <script src="./day26.js"></script>
    </body>
</html>
// arrow function
// var sum = (a,b) =>{
//     console.log("sum:",a+b);
// }
// sum(3,4);
// var sum=(a,b)=>console.log("sum:",sum) If there is a single line only ten curly braces are not required.
// sum(3,4);

// Array Methods

// var array = [1,2,3,4,5];

// // 1.map
// var newArray = array.map((data) => data*2);
// console.log("newArray " ,newArray,"index");


// If you are using {}then you need to use the "return"
// var newArray = array.map((data) => {return data*2});
// console.log(newArray);

// 2.Filter 
// var newArray=array.filter((data) => data>=3);
// console.log(newArray);
// Or
// var newArray=array.filter((data) => {
//  if(data>3){
//     return data;
// }
// });
// console.log(newArray);

// 3.Find
// var newArray=array.find((data)=>data>=2);
// console.log("Find",newArray);
// 

// 4.Reduce
// var totalSum=array.reduce((accumulation,currentvalue)=>accumulation*currentvalue);
// console.log("totalsum:",totalSum);

var FlipkartCart = [
    {
        price: 200,
        quantity:2
    },
    {
        price: 400,
        quantity:1
    },
    {
        price: 300,
        quantity:4
    },
    {
        price: 500,
        quantity:2
    },
    {
        price: 1000,
        quantity:3
    }
];
var totalCost=FlipkartCart.reduce((accumulator,currentValue) => {
    return accumulator + currentValue.price*currentValue.quantity},0);
console.log(totalCost);

// Promises
// It is an object that returns its value that we hope to execute in future not immediately
// 1.Pending State ()
// 2.Fullfill()
// 3.Reject()
// Syntax
// var myPromise=new Promise(()=>{})
// var myPromise=new Promise(function(){})
 
var myPromise=new Promise((resolve,reject)=>{
    setTimeout(function(){
        resolve("sucess");
    },5000);
    setTimeout(function(){
       reject("error occured"); 
    },7000); 
});
myPromise
.then((data)=>{console.log(data)})
.catch((err)=>{console.log(err)});
