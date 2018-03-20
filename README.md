
#### PROBLEM NAME : Simple Array Sum
#### AUTHOR : shashank21j
#### URL : https://www.hackerrank.com/challenges/simple-array-sum/problem
#### JAVASCRIPT CODE :

'use strict';

const fs = require('fs');

process.stdin.resume();

process.stdin.setEncoding('utf-8');

let inputString = '';

let currentLine = 0;

process.stdin.on('data', inputStdin => {

    inputString += inputStdin;

});

process.stdin.on('end', _ => {

    inputString = inputString.trim().split('\n').map(str => str.trim());

    main();
});

function readLine() {

    return inputString[currentLine++];

}

function simpleArraySum(n, ar) {

    let i;

    let x=0;

    for (i = 0; i < n; i++) {

  x= x+ar[i];

} 
    return x;

}

function main() {

    const ws = fs.createWriteStream(process.env.OUTPUT_PATH);

    const n = parseInt(readLine(), 10);

    const ar = readLine().split(' ').map(arTemp => parseInt(arTemp, 10));

    let result = simpleArraySum(n, ar);

    ws.write(result + "\n");

    ws.end();
}


#### PSEUDOCODE
input n = pick as integer from readLine input

input ar = pick as array from arTemp input

process :

function simpleArraySum :

define i as let

define x as let equals to 0

start loop for (i=0; i < n; i++)

do

  x = x value  + ar(array order i);

end for

    return x;

end function

define result as let equals to function simpleArraySum

output :

write result + "\n"

#### How to run the code :
1. copy the code to url 'https://www.hackerrank.com/challenges/simple-array-sum/problem' (make sure the code bar is empty)
2. paste the JAVASCRIPT CODE to the code bar
3. select "javascript(Node.js)" as the language
4. click Run Program Button at the bottom right of the code bar


