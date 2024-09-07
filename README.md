# Backend-Assignments// BASIC CALCULATOR
function calculate(num1, num2, operation) {
    if (num1 == null ||  num2 == null || isNaN(num1) || isNaN(num2)) {
        return "invalid numbers provided.";
    }
    if (! ['add', 'subtract', 'multiply', 'divide']) {
        return "invalid operations";
    }
    if (operation === 'add') {
        return num1 + num2;
    } else if (operation === 'subtract') {
        return num1 - num2;
    } else if (operation === 'multiply') {
        return num1 * num2;
    } else if (operation === 'divide') {
        if (num2 === 0) {
            return 'cannot divide by zero,';
        }
        return num1 / num2
    }
}

console.log(calculate(6, 8, 'add')); // output 14
console.log(calculate(6, 2, 'subtract')); // output 4
console.log(calculate(4, 6, 'multiply')); // output 24
console.log(calculate(9, 3, 'divide')); // output 3
console.log(calculate(6, 2, 'modulo')); // output undefined
console.log(calculate(null, 5, 'add')); // output invalid numbers provided
