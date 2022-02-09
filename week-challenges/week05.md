# Week challenges - Week05 💻
---
- Tuesday 2022-02-08
1. A Rule of Divisibility by 13
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
