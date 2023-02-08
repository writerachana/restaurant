# restaurant

// Define a menu object
const menu = {
  breakfast: {
    item1: {
      name: "Pancakes",
      price: 10.99
    },
    item2: {
      name: "Waffles",
      price: 12.99
    }
  },
  lunch: {
    item1: {
      name: "Sandwich",
      price: 7.99
    },
    item2: {
      name: "Salad",
      price: 9.99
    }
  }
};

// Define a function to calculate the total bill
function calculateBill(order) {
  let total = 0;
  for (let i = 0; i < order.length; i++) {
    const item = order[i];
    total += menu[item.meal][item.item].price;
  }
  return total;
}

// Define an order
const order = [  { meal: "breakfast", item: "item1" },  { meal: "lunch", item: "item2" }];

// Calculate the total bill
const total = calculateBill(order);
console.log("Total: $" + total);
