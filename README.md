# BIG BANG Number Generator

This script generates an array of numbers from 1 to 100, with replacements based on divisibility by 3 and 5. The goal is to predict when a "big bang" might happen based on the collision of prime numbers 3 and 5.

## Problem Overview:
- Numbers divisible by 3 are replaced with the word 'BIG'.
- Numbers divisible by 5 are replaced with the word 'BANG'.
- Numbers divisible by both 3 and 5 are replaced with the phrase 'BIGBANG'.
- All other numbers remain unchanged.

The result is saved to a file called 'output.json'.

## Prerequisites:
- Node.js must be installed on your machine.

## Running the Script:

### Step 1: Clone the Repository

git clone https://github.com/Tinez-LA/Versa-BigBang.git
cd Versa-BigBang

### Step 2: Install Dependencies

The script doesn't require any additional dependencies, but Node.js needs to be installed.

### Step 3: Run the Script

Execute the following command to run the script:

node bigbang.js

### Step 4: Output

After running the script, an 'output.json' file will be created in the current directory. The content will look like this:

["1", "2", "BIG", "4", "BANG", "BIG", "7", "8", "BIG", "BANG", "11", "BIG", "13", "14", "BIGBANG", ...]

The script will print the message:

The result has been saved to 'output.json'
