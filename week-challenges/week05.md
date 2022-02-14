# Week challenges - Week05 💻
---
- Thursday 2022-02-09
1. Tile Using Typescript
~~~
class Tile{
  value: number;
  letter: string;

  constructor(letter : string, value: number){
    this.value = value;
    this.letter = letter;
  }

  printTile(){
    console.log(`
      ==================
        Letter: ${ this.letter }
        Value: ${ this.value }
      ==================`);
  }//END FUNCTION

}
~~~
2. Time Using Typescript
~~~
class Time {
  hour : number;
  minute : number;
  seconds : number;

  constructor(hour:number, minute:number, seconds:number){
    this.hour = hour;
    this.minute = minute;
    this.seconds = seconds;
  }

  printTime(){
    console.log(`
      ==================
        Hours: ${ this.hour }
        Minutes: ${ this.minute  }
        Seconds: ${ this.seconds }
      ==================
    `);
  }

  getInSeconds() : number{
    const minutes  = this.hour * 60 + this.minute;
    return minutes * 60 + this.seconds;
  }
}
~~~
3. Rational Using Typescript
~~~
class Rational{

  numerator : number;
  denominator : number;

  constructor(numerator:number, denominator:number){
    this.numerator = numerator;
    this.denominator = denominator;
  }

  printRational(){
    console.log(`${ this.numerator } / ${ this.denominator }`);
  }

  invert(){
    [this.numerator, this.denominator] = [this.denominator, this.numerator];
  }

  toFloat(){
    console.log( this.numerator / this.denominator );
  }

  reduce(){
    let gcd = function gcd(a : number,b : number) : number{
    return b ? gcd(b, a%b) : a;
    };
    let gcd2 = gcd(this.numerator,this.denominator);
    this.numerator = this.numerator/gcd2;
    this.denominator = this.denominator/gcd2;
    // return [this.numerator/gcd2, this.denominator/gcd2];
  }

}//END class
~~~
4. Movies
~~~
DONE
~~~
- Wedesday 2022-02-08
6. Duplicate Encoder
~~~
export function duplicateEncode(word: string){
    return word.toLowerCase()
          .split('')
          .reduce((acc, char, i, arr) => {
            const symbol = arr.filter(letter => letter === char).length < 2 ? '(' : ')'
    
            return acc + symbol;
    }, '');
}
~~~
2. Find the Odd Int
~~~
export const findOdd = (xs: number[]): number => {
    return xs.reduce( (a,b)=> a^b);
};
~~~
3. Which are in?
~~~
function inArray(a1: string[], a2: string[]): string[] {
    let res : string[] = [];
    for(let i = 0; i < a1.length; i++){

        for(let j = 0; j < a2.length; j++){
            if( a2[j].includes(a1[i])){
                res.push(a1[i]);
            }
        }

    }//END FOR I

    return res.sort().filter(function(item, pos, ary) {
        return !pos || item != ary[pos - 1]; });
}
~~~
4. Sum of parts
~~~
export function partsSums(ls: number[]): number[] {
  let sum = ls.reduce((x, y) => x + y, 0);
  let resultArr = [];
  let x = 0;
  
  if(ls.length === 0) {
    return [0];
  }
  
  for(let i = 0; i <= ls.length; i += 1) {
    resultArr.push(sum);
    x = ls[i];
    sum -= x;
  }
  
  return resultArr;
  
  // let total = ls.reduce((acc, cur) => acc + cur, 0)
  //return [ ...[total], ...ls.map(num => total -= num) ]
}
~~~
5. Consecutive strings
~~~
export function longestConsec(strarr: string[], k: number): string {
  if (strarr.length == 0 || k > strarr.length || k <= 0) return '';
    
    let longStr : string = '';
    
    let newStr : string[] = [];
    
    for (let i = 0; i < strarr.length; i++){
      newStr = strarr.slice(i, i+k);
      if (newStr.join('').length > longStr.length ){
        longStr = newStr.join('');
      }
    }
    
    return longStr;
}
~~~
- Tuesday 2022-02-08
7. A Rule of Divisibility by 13
~~~
PENDING
~~~
2. Playing with digits
~~~
export class G964 {

    public static digPow = (n: number, p: number) => {
        let string = n.toString();
  let len = string.length;
  let result = 0;
  for(var i = 0; i < len ; i++) {
    var numberser = parseInt(string.charAt(i),10);
    result +=  Math.pow(numberser, p + i)
  }
  var x = Math.pow(n,p);
  if(result === x){
    return p;
    } else if(result%n === 0) {
    return result / n;
  }else {
    return -1  
}
~~~
3. Valid Braces
~~~
export function validBraces(braces: string): boolean {
   let brackets = "[]{}()<>"
  let stack = []

  for(let bracket of braces) {
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
4. Tic Tac Toe
~~~
PENDING
~~~
5. Tic Tac Toe Table Generator
~~~
function displayBoard(board, width){
let line = "-".repeat(3 * width + (width - 1));
  line = "\n" + line + "\n";
  console.log(line);
  let res = "";
  let breaks = [];
  for(let i = 0; i < (board.length / width) - 1; i++){
    breaks.push( Number((width * (i+1)) - 1 ));
  }
//   console.log(breaks);
  
  for(let i = 0; i < board.length; i++){
    res += ( board[i] != '') 
            ? " " + board[i] + " "
            : "   ";
    
    if(breaks.indexOf(i) >= 0){
//       console.log("In", i);
      res += line;
    }
    else{
//       console.log("NOT In");
      res += "|";
    }
  }
  return res.slice(0, -1);
}
~~~
- Monday 2022-02-07
7. Square(n) Sum at [Here](https://www.codewars.com/kata/515e271a311df0350d00000f/train/typescript) 
~~~
function squareSum(numbers: number[]): number {
    return numbers.reduce((prev, curr) => prev + curr * curr, 0);
}
~~~
2. Growth of a Population at [Here](https://www.codewars.com/kata/563b662a59afc2b5120000c6/train/typescript)  
~~~
export class G964 {

    public static nbYear = (p0, percent, aug, p) => {
        let years : number = 0;
        let pop : number = p0;
        while(pop < p){
            pop += pop * percent / 100 + aug;
            years ++;
        }
        return years;
    }
}
~~~
3. Mumbling at [Here](https://www.codewars.com/kata/5667e8f4e3f572a8f2000039/train/typescript)  
~~~
export function accum(s: string): string {
   return s.split('')
  .map((item, idx) => item.toUpperCase() + (item.toLowerCase()).repeat(idx))
  .join('-');
}
~~~
4. asdfsadf at
~~~
function warnTheSheep(queue: string[]): string {

    const position = queue.reverse().indexOf('wolf');
    return ( position > 0 ) ? `Oi! Sheep number ${position}! You are about to be eaten by a wolf!` : 'Pls go away and stop eating my sheep';
  
}
~~~
