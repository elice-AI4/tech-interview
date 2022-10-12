## map

### 직접 구현해보기

```js
const map01 = (array, func) => {
    let newArray = [];
    for (const item of array){
        const newValue = func(item);
        newArray.push(newValue);
    }
}

const map02 = (array, func) => {
    let newArray = [];
    for (let i=0; i<array.length; i++) {
        const newValue = func(array[i], i);
        newArray.push(newValue)
    }
}
```

### map 함수

```js
const exampleArray = [1, 2, 3];

const mappedResult = exampleArray.map((element) => {
    console.log(element);
    return element;
});
>>> 1
>>> 2
>>> 3

exampleArray === mappedResult; //false
```

> 같은 [1, 2, 3]인데도 false인 이유: reference인 Array는 새롭게 반환된 mappedResult에 새로운 주소값을 부여하기 때문에 둘은 같은 값이 아닙니다. <br> cf. primitive: string, number, bigint, boolean, undefined, symbol, null <br> cf. !primitive === Objects 사실상 primitive가 아닌 건 전부 reference(JS에서는 object)라 생각하면 됨

## filter

### 직접 구현해보기

```js
const filter01 = (array, func) => {
    let newArray = [];
    for (const item of array) {
        const isFiltered = func(item)
        if isFiltered === true {
            newArray.push(item)
        }
    }
    return newArray;
}

const filter02 = (array, func) => {
    let newArray = [];
    for (let i=0; i<array.length, i++) {
        if (func(array[i], i) === true) {
            newArray.push(array[i])
        }
    }
    return newArray;
}
```
### filter 함수

```js
const exampleArray = [1, 2, 3, 4, 5, 6]

const filteredArray = exampleArray.filter((element) => element % 2 === 0 );

console.log(filteredArray);

>>> [2, 4, 6]
```


## reduce

### 직접 구현하기

```js
const reduce01 = (array, func, initialValue) => {
    let result = initialValue;
    for (let i=0; i<array.length; i++) {
        result = func(result, array[i])
    }
    return result;
}
```

### reduce 함수

```js
const exampleArray = [1, 2, 3]

// reduce((누적값, 현잿값, 인덱스, 요소) => {return 결과}, 초깃값))

const reducedArray = exampleArray.reduce((acc, cur, i) => {
    console.log(acc, cur, i);
    return acc + cur
}, 0);

>>> 0 1 0
>>> 1 2 1
>>> 3 3 2
```