# Code_Challenge7.py
print("Welcome to the Grocery Program!")
print("We are delighted to have you here. Let's get started with your shopping experience.")
name = input("Please enter your name: ")

store_name = "Yes/No"
price_per_kg_pork = 250.00
amount_given = 1000

total_amount = 30.5 * price_per_kg_pork
change = amount_given - total_amount

if change < 0:
    print(f"Hi {name}, it seems you have insufficient funds. You need an additional {-change:.2f}php.")
else:
    print(f"Hi {name}, you purchased pork tenderloin with a total amount of {total_amount:.2f}php. Your change from {amount_given}php is {change:.2f}php.")

calculate_discount = lambda price, discount: price * (discount / 100)
calculate_tax = lambda price, tax: price * (tax / 100)

total_price = 2500.00
customer_age = 65

if customer_age >= 60:
    senior_discount = 5
else:
    senior_discount = 0

discounted_price = total_price - calculate_discount(total_price, senior_discount)
tax_rate = 12
total_price_with_tax = discounted_price + calculate_tax(discounted_price, tax_rate)

print(f"\nTotal Price: {total_price:.2f}php")
print(f"Senior Discount: {senior_discount}%")
print(f"Discounted Price: {discounted_price:.2f}php")
print(f"Tax Rate: {tax_rate}%")
print(f"Total Price with Tax: {total_price_with_tax:.2f}php")

print(f"\nThank you for shopping with us, {name}! Have a great day!")
