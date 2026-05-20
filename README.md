# Tarea_Python
Gestionar el menú de un restaurante

# MATRIZ DE PRODUCTOS
menu = [
    ["Arroz con tilapia frita", "Seco", 15000],
    ["Arroz con res", "Seco", 16000],
    ["Mondongo", "Sopa", 15000],
    ["Pescado", "Sopa", 17000],
    ["Hamburguesa Grande", "Comida rápida", 12000],
    ["Helado de vainilla", "Postre", 5000]
]

# DATOS DE LA PROMOCIÓN
categoria_objetivo = "Seco"
umbral = 12000

# FUNCIÓN
def calcular_precio_final(categoria, precio):
    
    if categoria == categoria_objetivo and precio > umbral:
        descuento = precio * 0.15
        precio_final = precio - descuento
    else:
        precio_final = precio
        
    return precio_final

# PROCESO Y SALIDA
print("------ MENÚ CON PROMOCIÓN ------")

for producto in menu:
    
    nombre = producto[0]
    categoria = producto[1]
    precio_base = producto[2]
    
    precio_final = calcular_precio_final(categoria, precio_base)
    
    print("\nProducto:", nombre)
    print("Categoría:", categoria)
    print("Precio base: $", precio_base)
    print("Precio final: $", precio_final)

  

