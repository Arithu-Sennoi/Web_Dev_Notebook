using a period(`.`) in regex pattern signifies that, the there could be any charecter at that postition. For example, `/gu./` will match with gun, gua, gus, gu1, gu4, anything. There could be literally any charecter as the third letter, which is the postion of the `.` in our regex pattern. 
```js
let humStr = "I'll hum a song";
let hugStr = "Bear hug";
let huRegex = /hu./;
huRegex.test(humStr);
huRegex.test(hugStr);
```

Both of these `test` calls would return `true`.

