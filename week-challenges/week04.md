# Week challenges - Week04 💻
---
- Thursday 2022-02-03
1. Detect Pangram
~~~
function isPangram(string){
  string = string.toLowerCase();
  return "abcdefghijklmnopqrstuvwxyz"
    .split("").every(function(x){
      return string.indexOf(x) !== -1;
  });
}
~~~
2. Find the missing letter
~~~
function findMissingLetter(array)
{
  const str = "abcdefghijklmnopqrstuvwxyz";
  const str2arr = array.join("");
  for (var i = 0; i < str2arr.length; i++) {
    if (str2arr.charCodeAt(i + 1) - str2arr.charCodeAt(i) != 1) {
      return String.fromCharCode(str2arr.charCodeAt(i) + 1);
    }
  } 
}
~~~
3. Find the unique number
~~~
function findUniq(arr) {
  const x = arr.filter((elm) => elm === arr[0]);
  const y = arr.filter((elm) => elm !== arr[0]);
  
  return x.length > y.length ? y[0] : x[0]
}
~~~
4. Reverse or rotate?
~~~
function revrot(str, sz) {
     ln = str.length;
   if(sz < 1 || !str || sz > ln) return "";

   const test = s => Array.prototype.reduce.call(s, (acc, val) => acc + Number(val) ** 3, 0) % 2 === 0;
   const reverse = s => s.split("").reverse().join("");
   const rotate = s => s.slice(1) + s.slice(0, 1);

   let arr = [];
   for(let i = 0; i < ln; i += sz) arr.push(i+sz <= ln ? str.slice(i, i+sz) : "")
   return arr.map(x => test(x) ? reverse(x) : rotate(x)).join("");
}
~~~
5. What's Your Poison?
~~~
function find(rats) {
    let res = 0;
    for(let i = 0; i < rats.length; i++){
      res += Math.pow(2, rats[i]);
    }
  return res;
}
~~~
- Wednesday 2022-02-02
7. Array.diff
~~~
function arrayDiff(a, b) {
  return a.filter(x => !b.includes(x));
}
~~~
2. Create Phone Number
~~~
function createPhoneNumber(numbers){
  return numbers.join('').replace(/(\d{3})(\d{3})(\d{4})/, "($1) $2-$3");
}
~~~
3. Watch this
~~~
DONE
~~~
4. Watch this
~~~
DONE
~~~
5. Read this
~~~
DONE
~~~
6. Read this
~~~
DONE
~~~
7. Read this
~~~
DONE
~~~
- Tuesday 2022-02-01
9. This link is nice to have and read
~~~
DONE
~~~
2. Typescript object type
~~~
PENDING
~~~
3. Read this
~~~
DONE
~~~
4. Typescript union types
~~~
PENDING
~~~
5. Typescript in operator
~~~
PENDING
~~~
6. Find the Odd Int
~~~
function findOdd(A) {
  
  let count = 0;
  let arr = A.sort((a, b) => a - b);
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr.length; j++) {
      if (arr[i] == arr[j]) {
        count++;
      }
    }
    if (count % 2 !== 0) {
      return arr[i];
    }
  }
  
}
~~~
7. Stop gninnipS My sdroW!
~~~
function spinWords(string){
  return string.split(' ').map( (x) => {
    
    return ( x.length >= 5 ) 
      ? x.split(""). reverse(). join("")
    : x;
    
  } ).join(' ');
}
~~~
- Monday 2022-01-31
9. Check this video
~~~
DONE
~~~
2. Follow this video
~~~
DONE
~~~
3. Follow this guide
~~~
DONE
~~~
4. Check this video
~~~
DONE
~~~
5. Follow this video
~~~
DONE
~~~
6. Check this video
~~~
DONE
~~~
