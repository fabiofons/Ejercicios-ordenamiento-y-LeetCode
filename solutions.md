# Ejercicios Ordenamiento y LeetCode

### 1. Insertion Sort
```javascript
function insertionSort(arr) {
  for (let i = 0; i < arr.length; i++) {
    let save = arr[i];
    let j;
    for (j = i - 1; j >= 0 && arr[j] > save; j--){
      arr[j + 1] = arr[j]; 
    }
    arr[j + 1] = save;
  }  
  return arr;
}
```
Complejidad de **O(n^2)**


### 2. Selection Sort
```javascript
function selSort(arr) {
  for (let i = 0; i < arr.length-1; i++) {
    let minNum = arr[i]; 
    let swap = i;
    for (let j = i + 1; j < arr.length; j++) {
      if (minNum > arr[j]) {
        minNum = arr[j];
        swap = j;
      }
    }
    if (i !== swap) {
      const tmp = arr[i];
      arr[i] = minNum;
      arr[swap] = tmp;
  	  }
  }
  return arr;
}
```
Complejidad de **O(n^2)**


### 3. Bubble Sort
```javascript
function bubbleSort(arr){
  let flat;
  do {
    flat = false
    for(let i = 0; i < arr.length; i++) {     
      if (arr[i] > arr[i + 1]) {
        let value = arr[i];
        arr[i] = arr[i + 1];
        arr[i + 1] = value;
        flat = true;
      }     
    }  
  } while(flat)
  return arr;
}
```
Complejidad de **O(n^2)**


## Bonus

### 4.  toLowerCase (LeetCode)
```javascript
var toLowerCase = function(str) {
    const vowel = { A:'a',B:'b',C:'c',D:'d',E:'e',F:'f',G:'g',H:'h',I:'i',J:'j',K:'k',
                    L:'l',M:'m',N:'n',O:'o',P:'p',Q:'q',R:'r',S:'s',T:'t',U:'u',V:'v',
                    W:'w',X:'x',Y:'y',Z:'z'}
    let newStr = '';
    for(let i = 0; i < str.length; i++) {
        if(str[i] in vowel){
            newStr += vowel[str[i]];
        }else {
            newStr += str[i];
        }
    }
    return newStr;
};
```
Complejidad espacial y temporal de **O(n)**


### 5.  ReverseString (LeetCode)
```javascript
var reverseString = function(s) {
  for(let i = 0; i < Math.floor(s.length / 2); i++) {
    let num = s[i];
    s[i] = s[s.length - 1 - i];
    s[s.length - 1- i] = num;
  }
  return s;  
};
```
Complejidad espacial y temporal de **O(n)**
