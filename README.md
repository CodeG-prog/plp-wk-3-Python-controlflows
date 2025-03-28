# plp-wk-3-Python-controlflows
Creating discount_price function using if, elif and else properties in Python

def calculate_discount(price, discount_percent):
   
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
        return price

original_price = float(input("Enter the original price of the item: "))
discount_percentage = float(input("Enter the discount percentage (0-100): "))

# Ensure discount percentage is within valid range
final_price = calculate_discount(original_price, discount_percentage)

if discount_percentage >= 20:
    print(f"Final price after {discount_percentage}% discount: ${final_price:.2f}")
else:
    print(f"No discount applied as the discount percentage is less than 20%. Original price: ${original_price:.2f}")
