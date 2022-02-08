# Week challenges - Week05 💻
---
- Thursday 2022-02-07
1. Square(n) Sum at [Here](https://www.codewars.com/kata/515e271a311df0350d00000f/train/typescript) 
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
