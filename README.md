# Stock-price-calculator
This is a beginner-friendly Python script that calculates the total investment value based on a selected stock and quantity.

# code
stock_prices = {
    "AAPL": 180,
    "TSLA": 250,
    "MSFT": 320
}
stock = input("Enter stock symbol (AAPL/TSLA/MSFT): ").upper()
quantity = int(input("Enter quantity: "))
if stock in stock_prices:
    price = stock_prices[stock]
    total = price * quantity
    print(f"\n{stock} @ ${price} x {quantity} = ${total}")
else:
    print("Stock not found.")
    exit()
save = input("Save to file? (yes/no): ").lower()
if save == "yes":
    filename = "portfolio.txt"
    with open(filename, "w") as file:
        file.write(f"{stock} @ ${price} x {quantity} = ${total}\n")
    print(f"Saved to {filename}")
