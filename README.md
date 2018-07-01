function findLongestWordLength(str) {
  let arr = str.split('');
  let count = 0;
  let newArr = [];
  for (let i = 0; i< arr.length; i++){ 
    if ((arr[i+1] === ' ')||(i === arr.length-1)){
newArr.push(count);
count = 0;
    }
 else {  count++}
}
for (let j=0; j < newArr.length; j++){
if (newArr[j] > newArr[newArr.length-1]) {
  newArr.push(newArr[j]);
}
}
  return newArr[newArr.length-1];
}

console.log(findLongestWordLength("What if we try a super-long word such as otorhinolaryngology"));
