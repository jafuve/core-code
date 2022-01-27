# Week challenges - Week03 💻
---

- Thursday 2022-01-25
1. Fold an Array
~~~
function foldArray(array, runs)
{
  let r = [];
  let array2 = [...array];
  
  for(let i = 0; i < runs; i++){
    
    let res = [];
    
    while(array2.length > 0){

      if(array2.length === 1){
        res.push(array2[0]);
        array2.shift();
        
      }else{
        res.push( Number(array2[0]) + Number(array2[ array2.length-1 ]));
        array2.shift();
        array2.pop();
      }
      
    }

    array2 = res;
    r = res;
    
  }
    
  return r;
}
~~~
2. Encrypt this
~~~
var encryptThis = function(text) {
 return text.split(' ')
  .map(word => word
  .replace(/(^\w)(\w)(\w*)(\w$)/, `$1$4$3$2`)
  .replace(/^\w/, word.charCodeAt(0)))
  .join(' ');
}
~~~
3.Format a string of names like 'Bart, Lisa & Maggie'. (retired)
~~~
function list(names){
  return names.map(x => x.name).join(', ').replace(/, ([^,]*)$/, ' & $1');
}
~~~
- Wednesday 2022-01-25

1. Valid Parentheses
~~~
function validParentheses(parens) {
  let brackets = "[]{}()<>"
  let stack = []

  for(let bracket of parens) {
    let bracketsIndex = brackets.indexOf(bracket)

    if(bracketsIndex % 2 === 0) {
      stack.push(bracketsIndex + 1)
    } else {
      if(stack.pop() !== bracketsIndex) {
        return false;
      }
    }
  }
  return stack.length === 0
}
~~~

2. Convert string to camel case
~~~
function toCamelCase(str){
 function isUpperCase(str) {
    for (var i = 0, len = str.length; i < len; i++) {
        var letter = str.charAt(i);
        var keyCode = letter.charCodeAt(i);
        if (keyCode > 96 && keyCode < 123) {
            return false;
        }
    }

    return true;
}
  
  let copy = str;
  let res = copy.split(/_|-/)
            .map( str => str.charAt(0).toUpperCase() + str.slice(1) )
            .join('');
  
  return ( isUpperCase(str.charAt(0)) )
          ? res 
          :  res.charAt(0).toLowerCase() + res.slice(1);
}
~~~
3. Unique in Order
~~~
var uniqueInOrder=function(iterable){
  let res = [];
  
  let newArray = (typeof(iterable) == "string") ? Array.from(iterable) : iterable;
  
  let c = "";
  for(let i = 0; i < newArray.length; i++){
      if(c != newArray[i]){
        res.push(newArray[i]);
        c = newArray[i];
      }
  }
  
  return (newArray.length == 1) ? newArray : res;
}
~~~
Tuesday 2022-01-24
1. You order, please
~~~
function order(words){
   return words.split(' ')
                .sort(function(a,b){
                        return a.match(/\d/) - b.match(/\d/);
                }).join(' ');
}
~~~
2. Duplicate count
~~~
function duplicateCount(text){
   return (text.toLowerCase().split('').sort().join('').match(/([^])\1+/g) || []).length;
}
~~~
3. 
Simple Pig Latin
~~~
function pigIt(str){
  const a1 = str.split(' ');
  var regP = /[,!?@#$%^&*()\u9999]/;
  return a1.map(x => 
                ( x.match(regP) )
                ? x 
                : (x.substring(1, x.length) + x.substring(0, 1)) + "ay"
               ).join(' ');
}
~~~
Monday 2922-01-24

1. Who likes it
~~~
function likes(names) {
  if(names.length == 0)
    return "no one likes this";
  else if(names.length == 1)
    return names[0] + " likes this";
  else if(names.length == 2)
    return names[0] + " and " + names[1] + " like this";
  else if(names.length == 3)
    return names[0] + ", " + names[1] + " and " + names[2] + " like this";
  else 
    return names[0] + ", " + names[1] + " and " + ( names.length - 2 ) + " others like this";
}
~~~
2. Bit Counting
~~~
var countBits = function(n) {
  return Array.from(String(n.toString(2)), Number).filter(x => x > 0).length;
};
~~~
3. Decode the Morse code
~~~
decodeMorse = function(morseCode){
  const data = morseCode.trim().split('   ');
  let res = [];

  for (let i = 0; i < data.length; i++) {
    let temp = data[i].split(' ');
    for (let j = 0; j < temp.length; j++) {
      if (MORSE_CODE[temp[j]]) {
        res.push(MORSE_CODE[temp[j]]);
      }
    }//END FOR
    
    if (i !== data.length - 1) {
      res.push(' ');
    }//END IF
  }//END FOR
  return res.join('');
}
~~~
