# Week challenges - Week02 💻
---
Thursday 2922-01-20

1. http
~~~
function remove(s){
let arr =[]
  for (let i = s.length-1; i => 0; i--){
    if(s[i] != '!'){
      arr.push(s.slice(0,i+1));
      return arr.join('');
    }  
  }
}
~~~
2. http
~~~
function shortcut (string) {
  return string.replace(/[aeiou]/ig,'');
}
~~~
3. http
~~~
const rps = (p1, p2) => {
  if(p1 == p2)
    return 'Draw!';
  else if(p1 == 'rock' && p2 == 'scissors')
    return 'Player 1 won!';
  else if(p1 == 'rock' && p2 == 'paper')
    return 'Player 2 won!';
  else if(p1 == 'scissors' && p2 == 'rock')
    return 'Player 2 won!';
  else if(p1 == 'scissors' && p2 == 'paper')
    return 'Player 1 won!';
  else if(p1 == 'paper' && p2 == 'rock')
    return 'Player 1 won!';
  else if(p1 == 'paper' && p2 == 'scissors')
    return 'Player 2 won!';
};
~~~
4. http
~~~
function persistence(num) {
  function multiply(n){
    return n.reduce(function(a,b){return a*b;});
  }
  var count =0; 
    
  while(num.toString().length > 1) {
    num= num.toString().split("");
    num = multiply(num);
    count++;
  }
  return count;
}
~~~
---
Wednesday 2022-01-19
---
1. http
~~~
function dutyFree(normPrice, discount, hol){
  return Math.floor( hol / ( normPrice * (discount / 100) ) );
}
~~~
2. http
~~~
function twiceAsOld(dadYearsOld, sonYearsOld) {
  let tempDadAge = dadYearsOld;
  let tempSonAge = sonYearsOld;
  let years = 0, i = 0;
  while(true || years == 200){
    if(tempDadAge / 2 == tempSonAge ){
      years = i;
      break;
    }else{
      tempDadAge++;
      tempSonAge++;
    }
    i++;
  }
  return years;
}
~~~
3. http
~~~
function validSpacing(s) {
  
  if( s.includes('  ') || s[0] == ' ' || s[s.length-1] == ' ' )
    return is_valid = false;
  
  return true;
}
~~~
4. http
~~~
function fakeBin(x){
  let fakebin = "";
  
  for(let i = 0; i < x.length; i++){
    fakebin += (Number(x[i]) < 5) ? "0" : "1";
  }
    return fakebin;
}
~~~
---
Tuesday 2022-01-18
---
1. https://www.codewars.com/kata/50654ddff44f800200000004
~~~
function multiply(a, b){
  return a * b
}
~~~
2. https://www.codewars.com/kata/572b6b2772a38bc1e700007a
~~~
function uniTotal (string) {
// total up dem unicodes!
  let uniTotal = 0;
  for(let i = 0; i < string.length; i++){
    uniTotal += Number( string.charCodeAt(i) );
  }
  return uniTotal;
}
~~~
3. https://www.codewars.com/kata/55ad04714f0b468e8200001c
~~~
function getChar(c){
  return String.fromCharCode(c);
}
~~~
4. https://www.codewars.com/kata/551f37452ff852b7bd000139
~~~
function addBinary(a,b) {
  const addition = a + b;
  return Number(addition).toString(2);
}
~~~
5. https://www.codewars.com/kata/5ad0d8356165e63c140014d4
~~~
function finalGrade (exam, projects) {
  let final_grade = 0;
  
  if(exam > 90 || projects > 10)
    final_grade = 100;
  else if(exam > 75 && projects >= 5)
    final_grade = 90;
  else if(exam > 50 && projects >= 2)
    final_grade = 75;
  
  return final_grade;
}
~~~
Monday 2022-01-17
---
1. Follow the github course, you can find it here
~~~
Done
~~~
2. Watch a video
~~~
Done
~~~
3. Read an article
~~~
Done
~~~
4. Create an account in Codewars
~~~
Done
~~~
