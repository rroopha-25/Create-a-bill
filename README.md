# Create-a-bill
# Program to create a bill

print("Welcome to ABC Store")
print("-" * 30)

items = []
prices = []

# Take input for items
while True:
    item = input("Enter item name (or 'done' to finish): ")
    if item.lower() == "done":
        break
    price = float(input(f"Enter price of {item}: $"))
    items.append(item)
    prices.append(price)

# Generate bill
print("\n----- BILL -----")
total = 0
for i in range(len(items)):
    print(f"{items[i]:20}  ${prices[i]:.2f}")
    total += prices[i]

# Calculate tax and total
tax = total * 0.08  # assuming 8% tax
grand_total = total + tax

print("-" * 30)
print(f"Subtotal:           ${total:.2f}")
print(f"Tax (8%):           ${tax:.2f}")
print(f"Total:              ${grand_total:.2f}")
print("-" * 30)
print("Thank you for shopping with us!")
