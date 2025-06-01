def km_to_miles(km): return km * 0.621371
def miles_to_km(mi): return mi / 0.621371
def c_to_f(c): return (c * 9/5) + 32
def f_to_c(f): return (f - 32) * 5/9
def kg_to_lb(kg): return kg * 2.20462
def lb_to_kg(lb): return lb / 2.20462

def main():
    while True:
        print("\n📐 Unit Converter")
        print("1. Kilometers to Miles")
        print("2. Miles to Kilometers")
        print("3. Celsius to Fahrenheit")
        print("4. Fahrenheit to Celsius")
        print("5. Kilograms to Pounds")
        print("6. Pounds to Kilograms")
        print("7. Quit")

        choice = input("Choose an option (1–7): ").strip()

        if choice == "7":
            print("👋 Goodbye!")
            break

        value = input("Enter the value: ").strip()
        try:
            val = float(value)
        except ValueError:
            print("❌ Invalid number.")
            continue

        if choice == "1":
            print(f"{val} km = {km_to_miles(val):.2f} miles")
        elif choice == "2":
            print(f"{val} miles = {miles_to_km(val):.2f} km")
        elif choice == "3":
            print(f"{val} °C = {c_to_f(val):.2f} °F")
        elif choice == "4":
            print(f"{val} °F = {f_to_c(val):.2f} °C")
        elif choice == "5":
            print(f"{val} kg = {kg_to_lb(val):.2f} lbs")
        elif choice == "6":
            print(f"{val} lbs = {lb_to_kg(val):.2f} kg")
        else:
            print("❌ Invalid option.")

if __name__ == "__main__":
    main()
