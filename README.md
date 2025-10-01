# Arube-s-programming
KIDEGANONO LAWRENCE
M25B13/025
// Function to calculate the total expenses
function calculateTotal(expenses) {
    let sum = 0;
    // Using a FOR loop to add up all expenses
    for (let i = 0; i < expenses.length; i++) {
        sum += expenses[i];
    }
    return sum;
}

// Function to check financial status based on budget
function checkBudget(total, budget) {
    // Using conditions to evaluate spending
    if (total < budget * 0.5) {
        return "You are doing great! Less than half your budget used.";
    } else if (total <= budget) {
        return "Careful! You are close to your budget limit.";
    } else {
        return "Warning! You have overspent your budget.";
    }
}

// MAIN PROGRAM
let dailyExpenses = [20, 15, 10, 30, 25]; // Example expenses in dollars
let budget = 100; // Daily budget

// Calculate total expenses
let totalSpent = calculateTotal(dailyExpenses);

// Check budget status
let status = checkBudget(totalSpent, budget);

// Display results
console.log("Expenses: " + dailyExpenses);
console.log("Total Spent: $" + totalSpent);
console.log("Budget: $" + budget);
console.log("Status: " + status);

// Extra feature: simulate expenses over a week using WHILE loop
let weeklyExpenses = [
    [20, 15, 10],    // Day 1
    [25, 30, 20],    // Day 2
    [10, 5, 15],     // Day 3
    [50, 20, 30],    // Day 4
    [5, 10, 5],      // Day 5
    [40, 20, 15],    // Day 6
    [30, 25, 10]     // Day 7
];

let day = 0;
while (day < weeklyExpenses.length) {
    let dayTotal = calculateTotal(weeklyExpenses[day]);
    console.log(`Day ${day + 1}: Spent $${dayTotal} - ${checkBudget(dayTotal, budget)}`);
    day++;
}
