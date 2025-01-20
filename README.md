# Importamos librerías para hacerlo más interesante
import time
import random
import textwrap

# Función para crear una línea separadora bonita
def imprimir_linea():
    print("=" * 50)

# Función para darle estilo al texto "Hola Mundo"
def hola_mundo_estilizado():
    imprimir_linea()
    print("🌍 Bienvenidos al programa de 'Hola Mundo' 🌟")
    imprimir_linea()
    print("\n" * 2)
    time.sleep(1)

    mensaje = "HOLA MUNDO"
    decoracion = ["*", "-", "~", "+", "="]

    for i in range(5):
        decorador = random.choice(decoracion)
        print(decorador * 20 + " " + mensaje + " " + decorador * 20)
        time.sleep(0.5)

    print("\n" * 2)
    imprimir_linea()

# Función que explica qué es "Hola Mundo"
def explicar_hola_mundo():
    descripcion = """
    "Hola Mundo" es típicamente el primer programa que los desarrolladores
    escriben cuando están aprendiendo un nuevo lenguaje de programación.
    Representa un inicio simbólico en el mundo de la programación.
    """
    print(textwrap.fill(descripcion, width=70))
    imprimir_linea()
    time.sleep(1)

# Función interactiva con el usuario
def interactuar_con_usuario():
    print("¿Quieres aprender a decir 'Hola Mundo' en otros idiomas? (sí/no)")
    respuesta = input("Escribe tu respuesta aquí: ").strip().lower()

    if respuesta == "sí":
        otros_idiomas()
    elif respuesta == "no":
        print("¡Está bien! ¡El mensaje universal es suficiente!")
    else:
        print("No entendí tu respuesta, pero igual te deseo un excelente día.")

# Función para mostrar "Hola Mundo" en otros idiomas
def otros_idiomas():
    idiomas = {
        "Inglés": "Hello, World!",
        "Francés": "Bonjour, le monde!",
        "Alemán": "Hallo, Welt!",
        "Italiano": "Ciao, Mondo!",
        "Portugués": "Olá, Mundo!",
        "Chino": "你好，世界！",
        "Japonés": "こんにちは、世界！",
        "Ruso": "Привет, мир!",
        "Hindi": "नमस्ते दुनिया!",
        "Árabe": "مرحبا بالعالم!"
    }

    print("\nAquí tienes 'Hola Mundo' en otros idiomas:\n")
    for idioma, traduccion in idiomas.items():
        print(f"{idioma}: {traduccion}")
        time.sleep(0.5)

# Función principal
def main():
    hola_mundo_estilizado()
    explicar_hola_mundo()
    interactuar_con_usuario()
    print("\n¡Gracias por visitar este programa de 'Hola Mundo'! 🌟")

# Llamada al programa principal
if __name__ == "__main__":
    main()
