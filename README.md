## README: Predicting the Big Bang with Prime Numbers

### This script generates an array of numbers from 1 to 100, replacing numbers divisible by 3 with "BIG", numbers divisible by 5 with "BANG", and numbers divisible by both 3 and 5 with "BIGBANG". The result is saved in a JSON file called 'output.json'.

### (1) Importing the 'fs' Module

const fs = require('fs');

This line imports the 'fs' (file system) module, which allows us to interact with the file system, in this case, to save the result to a file.

### (2) Initializing an Empty Array

let result = [];

This line initializes an empty array called 'result', which will store the numbers or words (number, "BIG", "BANG", "BIGBANG") based on the given conditions.

### (3) Loop to Iterate Through Numbers from 1 to 100

for (let i = 1; i <= 100; i++) {

This 'for' loop iterates through the numbers from 1 to 100.

### (4) Checking for Divisibility by 3 and 5 (BIGBANG)

if (i % 3 === 0 && i % 5 === 0) {
  result.push("BIGBANG");
}

This block checks if 'i' is divisible by both 3 and 5. If true, "BIGBANG" is added to the 'result' array.

### (5) Checking for Divisibility by 3 (BIG)

else if (i % 3 === 0) {
  result.push("BIG");
}

This block checks if 'i' is divisible by 3. If true, "BIG" is added to the 'result' array.

### (6) Checking for Divisibility by 5 (BANG)

else if (i % 5 === 0) {
  result.push("BANG");
}

This block checks if 'i' is divisible by 5. If true, "BANG" is added to the 'result' array.

### (7) Handling Other Numbers

else {
  let str = i.toString();
  result.push(str);
}

If none of the previous conditions are met (meaning 'i' is not divisible by 3 or 5), this block converts 'i' to a string and adds it to the 'result' array.

### (8) Writing the Result to a JSON File

fs.writeFileSync('output.json', JSON.stringify(result));

This line uses the 'writeFileSync' method from the 'fs' module to save the 'result' array as a JSON file called 'output.json'. The array is converted to a JSON string using 'JSON.stringify()'.

### (9) Console Output

console.log("The result has been saved to 'output.json'");

This line outputs a message to the console, confirming that the result has been saved to the 'output.json' file.

### How to Run the Script

1. Clone the repository or download the script.
2. Ensure you have Node.js installed.
3. Open a terminal or command prompt in the directory where the script is located.
4. Run the script with the following command: "node bigbang.js"
   
5. After the script runs, you will see a confirmation message in the console, and the 'output.json' file will be generated in the same directory.
