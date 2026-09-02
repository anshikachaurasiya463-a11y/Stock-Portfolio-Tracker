# Stock-Portfolio-Tracker
stock_prices = {
    "AAPL": 180,
    "TSLA": 250,
    "GOOGL": 140,
    "AMZN": 170,
    "MSFT": 420
}

total_investment = 0

print("📈 Stock Portfolio Tracker")
print("Available stocks:", ", ".join(stock_prices.keys()))

while True:
    stock = input("\nEnter stock name (or 'done' to finish): ").upper()

    if stock == "DONE":
        break

    if stock not in stock_prices:
        print("❌ Stock not available.")
        continue

    quantity = int(input("Enter quantity: "))

    value = stock_prices[stock] * quantity
    total_investment += value

    print("Stock:", stock)
    print("Quantity:", quantity)
    print("Investment:", value)

print("\n-------------------------")
print("Total Investment =", total_investment)
print("-------------------------")
