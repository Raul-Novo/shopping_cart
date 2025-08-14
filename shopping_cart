# Diccionario para guardar los productos y precios
cart: dict[str, float] = {}

def add_item(product_name: str, product_price: float) -> None:
    """Añade un producto con su precio a la cesta."""
    cart[product_name] = product_price
    print(f"'{product_name}' añadido a la cesta ({product_price:.2f}€)")

def show_cart() -> None:
    """Muestra todos los productos en la cesta."""
    if not cart:
        print("La cesta está vacía.")
        return

    print("\nTu cesta de la compra:")
    for name, price in cart.items():
        print(f" - {name:<15} {price:10.2f}€")

def main() -> None:
    """Ejecuta la lógica principal del programa."""
    print("=== Bienvenido a la cesta de la compra ===")

    while True:
        choice: str = input("\n¿Quieres añadir un producto? (S/N): ").strip().lower()

        # Validar opción del usuario
        if choice not in ("s", "n"):
            print("Opción inválida. Escribe 'S' o 'N'.")
            continue

        if choice == "n":
            print("\nGracias por usar la cesta. ¡Hasta luego!")
            show_cart()
            break

        # Pedir datos del producto
        product_name: str = input("Introduce el nombre del producto: ").strip()

        try:
            product_price = float(input("Introduce el precio (€): ").strip())
        except ValueError:
            print("Precio inválido. Se establecerá a 0€.")
            product_price = 0.0

        add_item(product_name, product_price)

if __name__ == "__main__":
    main()
