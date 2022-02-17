# Week challenges - Week06 💻
---
- Wednesday 2022-02-16
1. Build Tower Using Typescript
~~~
export const towerBuilder = (nFloors: number): string[] => {
 let res : string[] = [];
  
  for(let i = 1; i <= nFloors; i++){
    
    res.push( " ".repeat(nFloors - i) + "*".repeat(2 * i - 1) + " ".repeat(nFloors - i) );
    
  }
  
  return res;
  
}
~~~
2. Highest Scoring Word Using Typescript
~~~
export const high = (str: string): string =>{
  var words = str.split(' '),
      mx = 0,
      res = '';
  for(let i = 0; i < words.length; i++){
    var s = words[i],
        val = 0;
    for(let j = 0; j < s.length; j++){
      val += (s.charCodeAt(j) - 96);
    }
    if(val > mx){
      mx = val;
      res = s;
    }
  }
  return res;
}
~~~
3. Equal Sides Of An Array
~~~
export function findEvenIndex(arr: number[]): number
{
    var sum = 0,
    leftSum = 0;

  for (var i = 0; i < arr.length; i++) {
    sum += arr[i];
  }

  for (var i = 0; i < arr.length; i++) {
    sum -= arr[i];

    if (leftSum === sum) {
      return i;
    }

    leftSum += arr[i];
  }

  return -1;
}
~~~
4. Meeting Using Typescript
~~~
PENDING
~~~
5. Street Fighter 2 - Character Selection
~~~
export function streetFighterSelection(fighters: Array<string[]>, position: number[], moves: string[]) {
    let hoveredCharacters = [];
  let currentPosition = position;
  for (let move of moves){

    if (move == 'up'){
      if(currentPosition[0] == 0){
        hoveredCharacters.push(fighters[currentPosition[0]][currentPosition[1]]);
      } else{
        currentPosition[0]--;
        hoveredCharacters.push(fighters[currentPosition[0]][currentPosition[1]]);
      }
    }
    
    if (move == 'down'){
      if(currentPosition[0] == 1){
        hoveredCharacters.push(fighters[currentPosition[0]][currentPosition[1]]);
      } else{
        currentPosition[0]++;
        hoveredCharacters.push(fighters[currentPosition[0]][currentPosition[1]]);
      }
    }
    
    if (move == 'left'){
      if(currentPosition[1] == 0){
        currentPosition[1] = 5;
        hoveredCharacters.push(fighters[currentPosition[0]][currentPosition[1]]);
      } else{
        currentPosition[1]--;
        hoveredCharacters.push(fighters[currentPosition[0]][currentPosition[1]]);
      }
    }
    
    if (move == 'right'){
      if(currentPosition[1] == 5){
        currentPosition[1] = 0;
        hoveredCharacters.push(fighters[currentPosition[0]][currentPosition[1]]);
      } else{
        currentPosition[1]++;
        hoveredCharacters.push(fighters[currentPosition[0]][currentPosition[1]]);
      }
    }
    
  }
  
  return hoveredCharacters;
}
~~~
- Monday 2022-02-14
7. Read this
~~~
DONE
~~~
2. Menu Using Typescript
~~~
DONE
~~~
- Tuesday 2022-02-15
1. Movies Using Typescript
~~~
DONE
~~~
2. Readme
~~~
PENDING
~~~
3. Interfaces
~~~
DONE
~~~
