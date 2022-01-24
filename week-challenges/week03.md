# Week challenges - Week03 💻
---
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
