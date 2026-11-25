# Menú de restaurante con promoción

# Matriz del menú: [Nombre del producto, Categoría, Precio base]
menu = [
    ["churrasco gratinado",  "Platos fuertes", 54000],
    ["Espaguetti Carbonara", "Platos fuertes", 30000],
    ["Ensalada Griega",      "Entradas",       13000],
    ["Sopa del día",         "Entradas",        9000],
    ["Limonada de coco",     "Bebidas",        11000],
    ["Brownie con helado",   "Postres",        14000],
    ["Cheesecake",           "Postres",        16000],
]

# Parámetros de la promoción
CATEGORIA_OBJETIVO = "Postres"
UMBRAL = 15000
DESCUENTO = 0.15  # 15 %


def calcular_precio_final(categoria, precio_base):
    """
    Devuelve el precio final de un producto.
    Aplica 15 % de descuento si la categoría es el objetivo
    y el precio base es mayor al umbral.
    """
    if categoria == CATEGORIA_OBJETIVO and precio_base > UMBRAL:
        return precio_base * (1 - DESCUENTO)
    return precio_base


def mostrar_menu(matriz):
    print(f"Promoción: {int(DESCUENTO * 100)}% en '{CATEGORIA_OBJETIVO}' "
          f"con precio base mayor a ${UMBRAL:,}\n")
    print(f"{'Producto':<22}{'Precio base':>14}{'Precio final':>16}")
    print("-" * 52)

    for nombre, categoria, precio_base in matriz:
        precio_final = calcular_precio_final(categoria, precio_base)
        marca = "  (promo)" if precio_final < precio_base else ""
        base_txt = f"${precio_base:,.0f}"
        final_txt = f"${precio_final:,.0f}"
        print(f"{nombre:<22}{base_txt:>14}{final_txt:>16}{marca}")


# Programa principal
mostrar_menu(menu)