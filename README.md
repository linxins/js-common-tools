#js-common-tools

JS ES6 writing tools based on function


## Functions

```javascript
import * as JSCT from 'js-common-tools'
```

### Array
- arrayUnique
  
  Array de emphasis<br>
```javascript
  arr.arrayUnique()
  JSCT.arrayUnique(arr)
```  
  
- arrayQuickSort

  Array sort (fast) <br>
  'asc': Ascending (default) <br>
  'desc': Descending
```javascript
   arr.arrayQuickSort('desc') 
   JSCT.arrayQuickSort(arr, 'desc')
```
  
- isNullOrEmpty

  Checks value if it has value or not. Returns true if it is null or undefined You can do recursive check.<br>
```javascript
   JSCT.isNullOrEmpty([]) // true
   JSCT.isNullOrEmpty([""]) // false
   JSCT.isNullOrEmpty([""], true) // true (Recursive check)
```    
- isArray 

  To determine whether the array <br>
```javascript
   JSCT.isArray(value)
```

- inArray

  check needle value in array<br>
```javascript
  JSCT.inArray(1, ['1', 'ss'], true) // false
  JSCT.inArray(1, [1, 'ss'], true) // true
```

### Number
- getRandomInt

  To obtain the specified interval of random integers, default 1 to 100 <br>
```javascript
   JSCT.getRandomInt(1, 20)
```
  
- toFixedDecimal
  
  Returns fixed decimal number<br>
```javascript
  JSCT.toFixedDecimal(1.689442324, 2) // 1.68
```

### String
- trimAll 
  
  Clear all spaces in character <br>
```javascript
  str.trimAll()
```
  
- trimL 
  
  Clear left space <br>
```javascript
  str.trimL()
``` 
- trimR 

  Clear right space in character <br>
```javascript
  str.trimR()
``` 
- getUUID
  
  Return a unique identifier with the given len.<br>
```javascript
  JSCT.getUUID(20, true) or JSCT.getUUID()
```

- sprintf
  
```javascript
  JSCT.sprintf('this values, num1: %s , num2: %s , num3: %s', 1, 2, 3)
  // this values, num1: 1 , num2: 2 , num3: 3
```
- isCreditCard
  
```javascript
  JSCT.isCreditCard('5212345678901234') // true
```

- isEmail 
  
```javascript
  JSCT.isEmail('liufulin90@163.com') // true
``` 
 
  
- isUrl 
  
```javascript
  JSCT.isUrl('http://www.linxins.com') // true
```  
  
 
- isIdentityCard

  To determine whether the Chinese identity card number<br>
```javascript
  JSCT.isIdentityCard('231421199406042025') // false
  // ps: Enter the Chinese identity card number to do the test, return to true
```
### Other
- cookie

   get and set cookie<br>
```javascript
  // set 
  JSCT.cookie('test', '123')
  // get
  JSCT.cookie('test') // 123
```

- store
   
```javascript
   JSCT.getLocalStorage(key)
   JSCT.setLocalStorage(key, value)
   JSCT.getSessionStorage(key)
   JSCT.setSessionStorage(key, value)
``` 
  
- Timer

  This is a timer tool
```javascript
  let tt = new JSCT.Timer()
  tt.start(function (timeStr) {
    console.log(timeStr)// do something. ret: 00:03:35
  })
  setTimeout(()=>{
    tt.stop()
  }, 3000)
```
  
## Installation

via npm:

```bash
$ npm install js-common-tools
```

## License
(The MIT License)

Copyright (c) 2016 linxins <liufulin90@163.com>
