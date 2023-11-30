# Casino Virtual

° Nicolás Antonio Sánchez Bautista
° Manuel Arturo Fajardo Contreras
° Juan David García Barreto

## ¿Cuál es el propósito de nuestro proyecto?

Proporcionar un entorno virtual dónde las personas puedan disfrutar de la emoción de un casino desde la comodidad de sus hogares.
Esto, además de permitirle a las personas tener una experiencia divertida y relajante, estableció un ambiente ideal para que el equipo de trabajo pudiera explorar las diferentes funcionalidades y herramientas de un lenguaje de programación tan amplio como lo es Python. 

![image](https://github.com/NicolasSanchez09/Casino-Virtual/assets/145717659/6fab8ecf-299d-453a-89c3-74a1793ed000)

Antes de iniciar, se definieron todos los juegos a desarrollar.

Tras unas cuantas conversaciones sobre cuáles serían más desafiantes y divertidos, se seleccionaron 5.

El primero de todos, una incorporación novedosa, pero muy intrigante. Se llama 'Agalludo'. Para los que no conocen de su existencia, este juego consiste en lanzar un dado hasta que se crea que va a salir '1'. En ese momento, el jugador decide guardar su puntaje, para ir acercándose a una meta. De lo contrario, si continua hasta que se tope con el número temido por todos, el jugador perderá todo lo acumulado en esa ronda.

![image](https://github.com/NicolasSanchez09/Casino-Virtual/assets/145717659/7a419d6f-aae5-4abf-82c0-1c304edbfde1)

Para el segundo, cómo no podría faltar, un clásico. Se incluyó 'BlackJack'. El juego que todos conocen donde el propósito es acercarse lo máximo posible al número '21' sin superarlo, con al menos dos cartas iniciales.

![image](https://github.com/NicolasSanchez09/Casino-Virtual/assets/145717659/7a552b67-7bc7-4bd1-ac61-746a30a83270)

En la tercera selección, se tomó la alternativa sencilla. El 'Tragamonedas'. Como todo ser humano sabrá, hay que girar las ruletas, esperando con el mayor de los deseos que todos los símbolos coincidan para obtener un gran premio.

![image](https://github.com/NicolasSanchez09/Casino-Virtual/assets/145717659/3bf860c2-b8e9-4c63-aa3e-d7bbb59c6324)


En el cuarto se optó por el niño más amado de los abuelos. El 'BINGO'. A pesar de su fama principalmente en adultos mayores, este juego invita a todas las edades para compartir en familia. Con el objetivo de hacerlo más dinámico, en vez del formato normal con las 5 letras y 75 números, se planteó uno llamado 'NMD' (por las iniciales de los integrantes). Para jugarlo, hay que completar una tabla de 3 x 3, en el que cada letra tiene su propio rango, y los números van desde el 1 hasta el 18. (N): 1-6; (M): 7-12; (D): 13-18. 

![image](https://github.com/NicolasSanchez09/Casino-Virtual/assets/145717659/62bdb206-99fd-4d52-b4e8-e2be9bf7f5b7)

Finalmente, para completar el quinteto inicial, se eligió el rey. Así es, la 'Ruleta'. Tan icónico como apasionante, en este juego se girará una gran ruleta, con diferentes casillas y posibilidades. Solo una de ellas esconde la posibilidad de hacer completamente millonario a un usuario afortunado.

![image](https://github.com/NicolasSanchez09/Casino-Virtual/assets/145717659/cf414b7e-fec1-4680-9bda-e3b362169307)

## ¿Cómo lo llevamos a cabo?

La idea inicial era hacer un juego en roblox studio. Este programa, como su nombre lo indica, es el motor de roblox, una plataforma de videojuegos en línea. Por medio de ella se puede diseñar desde el mapa en 3D, con todo tipo de detalles, hasta el sistema integrado de programación. Todo está basado en el lenguaje 'LUA', cuya sintáxis y facilidad es muy similar a Python.

En ese orden de ideas, en primer lugar, se diseñó un mapa con diferentes zonas para interactuar. Ahora bien, surgió un gran problema, puesto que para desarrollar un juego de este estilo, es necesario tener conocimientos sobre interfaces de usuario, interconectividad entre jugadores, datos guardados en la nube, comunicación con servidores físicos, y mucho más. Por lo cual, en vista de los conocimientos básicos, y naturalmente limitantes del equipo de trabajo, se optó por buscar otra alternativa más acorde a las posibilidades.

Fue allí cuando apareció la idea de realizar todo el sistema por medio de un cuaderno sencillo en google collaboratory. Esto facilitaría las diferentes interfaces, lo haría muy fácil de ubicar, pero, sobre todo, mantendría la esencia del proyecto de diversión y tranquilidad.

A continuación se adjuntará unas imagenes con el mapa diseñado inciailmente;

![image](https://github.com/NicolasSanchez09/Casino-Virtual/assets/145717659/2e5cdb7a-e94a-4ff7-ab8b-67f04f39b0e4)

![image](https://github.com/NicolasSanchez09/Casino-Virtual/assets/145717659/42d1ef0c-6d1e-4b4d-88d8-e1c2aa3a5eb3)

![image](https://github.com/NicolasSanchez09/Casino-Virtual/assets/145717659/0626d5a5-92e1-49cb-bc3b-b32863184cf1)

![image](https://github.com/NicolasSanchez09/Casino-Virtual/assets/145717659/f48466d5-3989-4555-910c-b386cd85c3d5)

![image](https://github.com/NicolasSanchez09/Casino-Virtual/assets/145717659/a4f35922-5e89-4e2a-9a9e-1f9e8e01083b)

Con todo nuevamente definido, fue hora de pasar a lo divertido... ¡¡La programación!!

## Resultado Final

En esta sección, se expondrá el código que se tiene que ejecutar para disfrutar del programa. Pero antes, es necesario comprender cómo hacer que funcione correctamente.

El primer paso es abrir el cuaderno compartido de google collaboratory. A continuación, se ejecutarán todas las secciones del programa una a una, hasta llegar a la 'Interfaz Principal'.

En ella, al correrla, el usuario podrá acceder a un menú con todas las opciones y detalles específicos.

Es fundamental ejecutar el programa en orden, para que la interfaz principal funcione correctamente.

## Importación e instalación de librerías

    %%capture
    import random
    from IPython.display import clear_output
    import time

## Agalludo

    def tirar_dado():
    return random.randint(1, 6)

    def jugar_agalludo():

        bucle_externo = True
        while bucle_externo:
            print("Bienvenido al juego 'Agalludo'")

            # Seleccionar la meta
            metas = [20, 50, 100, 250, 500, 1000]
            meta = int(input("Selecciona la meta (20, 50, 100, 250, 500, 1000): "))
            while meta not in metas:
                print("Meta no válida. Intenta de nuevo.")
                meta = int(input("Selecciona la meta (20, 50, 100, 250, 500, 1000): "))

            # Determinar quién empieza
            turno_inicial = random.choice(["Jugador", "Computadora"])
            print("(A): Jugador")
            print("(B): Computadora")
            print(f"Sorteo Inicial: {turno_inicial}")

            # Inicializar puntajes
            puntaje_jugador = 0
            puntaje_pc = 0

            while puntaje_jugador < meta and puntaje_pc < meta:
                if turno_inicial == "Jugador":
                    print("\nTurno del Jugador:")
                    puntaje_turno_jugador = 0

                    while True:
                        dado = tirar_dado()
                        print(f"Dado: {dado}")

                        if dado == 1:
                            print("¡Oh no! Has sacado un '1'. Pierdes el puntaje de este turno.")
                            puntaje_turno_jugador = 0
                            break
                        else:
                            puntaje_turno_jugador += dado
                            print(f"Puntaje de turno: {puntaje_turno_jugador}")

                        decision = input("Marca (1) para seguir o (2) para guardar: ")
                        if decision == "2":
                            break

                    puntaje_jugador += puntaje_turno_jugador
                    print(f"\nPuntaje acumulado del Jugador: {puntaje_jugador}")

                else:
                    print("\nTurno de la Computadora:")
                    puntaje_turno_pc = 0

                    while puntaje_turno_pc < 15:  # Decisión aleatoria de la computadora
                        dado = tirar_dado()
                        print(f"Dado: {dado}")

                        if dado == 1:
                            print("La Computadora ha sacado un '1'. Pierde el puntaje de este turno.")
                            puntaje_turno_pc = 0
                            break
                        else:
                            puntaje_turno_pc += dado
                            print(f"Puntaje de turno: {puntaje_turno_pc}")

                    puntaje_pc += puntaje_turno_pc
                    print(f"\nPuntaje acumulado de la Computadora: {puntaje_pc}")

                # Verificar si se ha alcanzado o superado la meta
                if puntaje_jugador >= meta or puntaje_pc >= meta:
                    break

                # Cambiar el turno
                turno_inicial = "Computadora" if turno_inicial == "Jugador" else "Jugador"

            # Mostrar el resultado final
            if puntaje_jugador >= meta:
                print("\n¡Felicidades! ¡Has ganado!")
            else:
                print("\n¡La Computadora ha ganado!")

            while True:
                respuesta = input("¿Quieres volver a jugar? (si/no): ")
                if respuesta == "si":
                    clear_output(wait=True)  # Limpia el tablero
                    time.sleep(1)  # Espera 1 segundo
                    print("Ok")
                    break
                elif respuesta == "no":
                    clear_output(wait=True)  # Limpia el tablero
                    time.sleep(1)  # Espera 1 segundo
                    print("Ok, gracias por jugar")
                    bucle_externo = False
                    break
                else:
                    clear_output(wait=True)  # Limpia el tablero
                    time.sleep(1)  # Espera 1 segundo
                    print("Respuesta no válida. Por favor, ingresa 'si' o 'no'.")

            time.sleep(1)  # Espera 1 segundo
            clear_output(wait=True)  # Limpia el tablero

## BlackJack

    #Programacion Juegoo blackjack...

    def jugar_blackjack(): #Cada que se quiera ingresar a esta zona, solo se llama esta funcion y listo
      bucle_externo = True
      while bucle_externo:
        # Función para crear una baraja estándar
        def crear_baraja():
            return ['2', '3', '4', '5', '6', '7', '8', '9', '10', 'J', 'Q', 'K', 'A'] * 4

        # Función para calcular el valor total de una mano de cartas
        def valor_carta(cartas):
            valor = 0
            ases = 0

            for carta in cartas:
                if carta in ['K', 'Q', 'J']:
                    valor += 10
                elif carta == 'A':
                    ases += 1
                else:
                    valor += int(carta)

            for _ in range(ases):
                if valor + 11 <= 21:
                    valor += 11
                else:
                    valor += 1

            return valor

        # Función para mostrar la mano de un jugador o del dealer
        def mostrar_mano(jugador, cartas, ocultar_segunda_carta=False):
          if ocultar_segunda_carta and jugador == "Dealer":
            cartas_mostradas = [cartas[0], 'X']
            print(f"Mano del {jugador}: {cartas_mostradas[0]} - Carta oculta")
          else:
            cartas_mostradas = cartas
            print(f"{jugador} mano: {' - '.join(cartas_mostradas)} (Valor: {valor_carta(cartas)})")

        # Función principal que implementa el juego de Blackjack
        def blackjack():
            # Inicializar la baraja y mezclar las cartas
            baraja = crear_baraja()
            random.shuffle(baraja)

            # Repartir cartas al jugador y al dealer
            jugador_mano = [baraja.pop(), baraja.pop()]
            dealer_mano = [baraja.pop(), baraja.pop()]

            while True:
                # Mostrar las manos
                mostrar_mano("Tu", jugador_mano)
                mostrar_mano("Dealer", dealer_mano, ocultar_segunda_carta=True)

                # Verificar si el jugador tiene Blackjack
                if valor_carta(jugador_mano) == 21:
                    print("¡Blackjack! ¡Ganaste!")
                    break

                # Verificar si el jugador se pasó de 21
                if valor_carta(jugador_mano) > 21:
                    print("Has perdido. Te has pasado de 21.")
                    break

                # Preguntar al jugador si quiere tomar otra carta
                decision = input("¿Quieres tomar otra carta? (si/no): ").lower()
                time.sleep(1)  # Espera 1 segundos
                clear_output(wait=True)

                # El bucle se activa solo si se ingresa una entrada invalidad
                while decision not in ['si', 'no']:
                    print("Entrada no válida. Por favor, ingresa 'si' o 'no'.")
                    decision = input("¿Quieres tomar otra carta? (si/no): ").lower()
                    time.sleep(1)  # Espera 1 segundos
                    clear_output(wait=True)

                # Tomar otra carta si el jugador decide hacerlo
                if decision == 'si':
                    jugador_mano.append(baraja.pop())
                else:
                    # El dealer toma cartas hasta que su mano tenga un valor de al menos 17
                    while valor_carta(dealer_mano) < 17:
                      if valor_carta(dealer_mano) < valor_carta(jugador_mano):
                        dealer_mano.append(baraja.pop())
                      else:
                        break

                    # Mostrar las manos después de que el jugador decide no tomar más cartas
                    mostrar_mano("Jugador", jugador_mano)
                    mostrar_mano("Dealer", dealer_mano)

                     # Determinar el resultado del juego
                    if valor_carta(dealer_mano) > 21:
                        print("¡Dealer se ha pasado de 21! ¡Ganaste!")
                    elif valor_carta(jugador_mano) > valor_carta(dealer_mano):
                        print("¡Ganaste!")
                    elif valor_carta(jugador_mano) < valor_carta(dealer_mano):
                        print("Perdiste. Dealer gana.")
                    else:
                        print("Empate.")

                    # Terminar el juego después de una ejecución
                    break
            # Mensaje de bienvenida y llamada a la función principal del juego
        print("Bienvenido a Blackjack.")
        time.sleep(2)  # Espera 2 segundos
        clear_output(wait=True)
        blackjack()
        while True:
          respuesta = input("Quieres volver a jugar? (si/no)")
          if respuesta == "si":
            clear_output(wait=True) #Limpia el tablero
            time.sleep(1)  # Espera 1 segundos
            print("ok")
            break

          elif respuesta == "no":
            clear_output(wait=True) #Limpia el tablero
            time.sleep(1)  # Espera 1 segundos
            print("ok, gracias por jugar")
            bucle_externo = False
            break

          else:
            clear_output(wait=True) #Limpia el tablero
            time.sleep(1)  # Espera 1 segundos

            print("Respuesta no válida. Por favor, ingresa 's' o 'n'.")

        time.sleep(1)  # Espera 1 segundos
        clear_output(wait=True) #Limpia el tablero

## Tragamonedas

     def jugar_tragamonedas():
      bucle_externo = True
      while bucle_externo:
        def tragamonedas():
            # Símbolos posibles en la tragamonedas
          simbolos = ['🍒', '🍊', '🍋', '🍇', '🍉', '🍓', '🍈', '🍍', '🔔', '💎']

          # Inicializar los tres rodillos con símbolos aleatorios
          rodillo1 = random.choice(simbolos)
          rodillo2 = random.choice(simbolos)
          rodillo3 = random.choice(simbolos)

            # Mostrar los resultados
          print(f"\n{' '.join([rodillo1])}\n")
          time.sleep(1)
          clear_output(wait=True)
          print(f"\n{' '.join([rodillo1, rodillo2,])}\n")
          time.sleep(1)
          clear_output(wait=True)
          print(f"\n{' '.join([rodillo1, rodillo2, rodillo3])}\n")
          time.sleep(1)

            # Verificar si hay coincidencias
          if rodillo1 == rodillo2 == rodillo3:
              print("¡Felicidades! Has ganado.")
          else:
              print("Lo siento, no hay coincidencias. Inténtalo de nuevo.")

        clear_output(wait=True)
        print("Bienvenido a tragamonedas.")
        time.sleep(2)  # Espera 2 segundos
        clear_output(wait=True)
        tragamonedas()
        while True:
          respuesta = input("Quieres volver a jugar? (si/no)")
          if respuesta == "si":
            clear_output(wait=True) #Limpia el tablero
            time.sleep(1)  # Espera 1 segundos
            print("ok")
            break

          elif respuesta == "no":
        clear_output(wait=True) #Limpia el tablero
        time.sleep(1)  # Espera 1 segundos
        print("ok, gracias por jugar")
        bucle_externo = False
        time.sleep(3)
        break

      else:
        clear_output(wait=True) #Limpia el tablero
        time.sleep(1)  # Espera 1 segundos
        print("Respuesta no válida. Por favor, ingresa 'si' o 'no'.")

      time.sleep(1)  # Espera 1 segundos
      clear_output(wait=True) #Limpia el tablero

## Bingo - (NMD)

    def jugar_bingo():
        bucle_externo = True
        while bucle_externo:
          def bingo ():
            # Función para generar un cartón de Bingo
            def generar_carton():
                carton = []
                letras = ['N', 'M', 'D']
                rangos = {'N': (1, 6), 'M': (7, 12), 'D': (13, 18)}

                for letra in letras:
                    columna = random.sample(range(rangos[letra][0], rangos[letra][1] + 1), 3)
                    carton.append(columna)

                return carton

            # Función para imprimir el tablero de Bingo
            def imprimir_tablero(tablero):
                for fila in tablero:
                    print(fila)

            # Función para evaluar el tablero después de sortear un número
            def evaluar_tablero(tablero, numero):
                for fila in range(len(tablero)):
                    for columna in range(len(tablero[fila])):
                        if tablero[fila][columna] == numero:
                            tablero[fila][columna] = 0

            # Función para verificar si hay un ganador en el tablero de Bingo
            def verificar_ganador(tablero):
                for fila in tablero:
                    if not all(num == 0 for num in fila):
                        return False
                return True

            # Generar cartones para el usuario y la computadora
            carton_usuario = generar_carton()
            carton_pc = generar_carton()

            # Conjunto para almacenar los números ya sorteados
            numeros_sorteados = set()

            # Imprimir los cartones iniciales
            print("Tu cartón:")
            imprimir_tablero(carton_usuario)

            print("\nCartón de la computadora:")
            imprimir_tablero(carton_pc)

            print("\nEmpecemos el juego\n")

            while True:
                # Preguntar al usuario si quiere continuar o abandonar
                decision = input("Presiona '1' para continuar, '2' para abandonar: ")

                if decision == '2':
                    confirmacion = input("Estás seguro de que quieres abandonar? Presiona '2' para confirmar, cualquier otra tecla para seguir: ")
                    if confirmacion == '2':
                        print("\nHas abandonado el juego. La computadora gana.")
                        break
                elif decision != '1':
                    print("Opción NO válida. Por favor, presiona '1' para continuar o '2' para abandonar.")
                    continue

                # Generar un número aleatorio que no haya salido
                while True:
                    numero_aleatorio = random.randint(1, 18)
                    if numero_aleatorio not in numeros_sorteados:
                        break

                # Agregar el número sorteado al conjunto
                numeros_sorteados.add(numero_aleatorio)

                print(f"Número sorteado: {numero_aleatorio}")

                # Evaluar y marcar el número en ambos cartones
                evaluar_tablero(carton_usuario, numero_aleatorio)
                evaluar_tablero(carton_pc, numero_aleatorio)

                # Imprimir los cartones actualizados
                print("\nTu cartón:")
                imprimir_tablero(carton_usuario)

                print("\nCartón de la computadora:")
                imprimir_tablero(carton_pc)

                # Verificar si hay un ganador
                if verificar_ganador(carton_usuario):
                    print("\n¡HAS GANADO!")
                    break
                elif verificar_ganador(carton_pc):
                    print("\nPERDISTE :(")
                    break
          print("Bienvenido al Bingo.")
          time.sleep(2)  # Espera 2 segundos
          clear_output(wait=True)
          bingo()
          while True:
            respuesta = input("¿Quieres volver a jugar? (si/no): ")
            if respuesta == "si":
                  clear_output(wait=True)  # Limpia el tablero
                  time.sleep(1)  # Espera 1 segundo
                  print("Ok")
                  break
            elif respuesta == "no":
                clear_output(wait=True)  # Limpia el tablero
                time.sleep(1)  # Espera 1 segundo
                print("Ok, gracias por jugar")
                bucle_externo = False
                break
            else:
                clear_output(wait=True)  # Limpia el tablero
                time.sleep(1)  # Espera 1 segundo
                print("Respuesta no válida. Por favor, ingresa 'si' o 'no'.")

          time.sleep(1)  # Espera 1 segundo
          clear_output(wait=True)  # Limpia el tablero

## Ruleta

    def girar_ruleta():
    return random.randint(1, 10)

    def obtener_premio(numero):
    premios = {
        1: "Ganas una tarjeta de regalo, redímela por 100 fichas",
        2: "Obtienes un descuento del 20% en el bar del casino",
        3: "Recibes un premio misterioso",
        4: "Ningún premio, inténtalo de nuevo",
        5: "Ganas una camiseta gratis, lleva la merch en la tienda del casino",
        6: "Obtienes un cupón de comida gratis",
        7: "Ganas un carro de carreras (Renault 4)",
        8: "Sigue intentando (jaja)",
        9: "Ganas un viaje a Melgar",
        10: "Obtienes licencia de un servicio útil para programar en grupo (no es colab)"
    }

    return premios.get(numero, "Error: número no válido")

    def jugar_ruleta():
    while True:
        input("Presiona Enter para girar la ruleta...")

        numero_ganador = girar_ruleta()

        print(f"La ruleta ha girado y el número ganador es: {numero_ganador}")

        premio = obtener_premio(numero_ganador)
        print(f"¡{premio}!")

        respuesta = input("¿Quieres volver a jugar? (si/no): ").lower()
        if respuesta != "si":
            print("¡Gracias por jugar! Hasta luego.")
            break

## Interfaz Principal

    print("Bienvenido al casino altamente adictivo")
    clear_output(wait=True)  # Limpia el tablero
    time.sleep(4)  # Espera 4 segundos
    print("Escoge el juego que gustes y recuerda que siempre que quieras irte, solo debes seleccionar la opcion 'salir'")
    clear_output(wait=True)
    time.sleep(7)

    while True:
        clear_output(wait=True)
        print("¿Qué juego deseas jugar? Recuerda que tenemos los siguientes:\n")

        # Organiza las opciones de juego en un diccionario y luego las imprime
        opciones_juegos = {
            1: ("Agalludo"),
            2: ("Blackjack"),
            3: ("Tragamonedas"),
            4: ("Bingo"),
            5: ("Ruleta"),
            6: ("Salir")
        }

    for clave, nombre in opciones_juegos.items():
        print(f"Clave: {clave}, Juego: {nombre}")

    eleccion = input("Para ingresar, escribe la clave del juego que deseas: ")

    try:
        eleccion = int(eleccion)

        if eleccion == 1:
            clear_output(wait=True)  # Limpia el tablero
            time.sleep(1)  # Espera 1 segundos
            jugar_agalludo()

        elif eleccion == 2:
            clear_output(wait=True)  # Limpia el tablero
            time.sleep(1)  # Espera 1 segundos
            jugar_blackjack()

        elif eleccion == 3:
            clear_output(wait=True)  # Limpia el tablero
            time.sleep(1)  # Espera 1 segundos
            jugar_tragamonedas()

        elif eleccion == 4:
            clear_output(wait=True)  # Limpia el tablero
            time.sleep(1)  # Espera 1 segundos
            jugar_bingo()

        elif eleccion == 5:
            clear_output(wait=True)  # Limpia el tablero
            time.sleep(1)  # Espera 1 segundos
            jugar_ruleta()
        elif eleccion == 6:
            print("Gracias por visitarnos, vuelve pronto :)")
            clear_output(wait=True)  # Limpia el tablero
            time.sleep(1)  # Espera 1 segundos
            break

    except ValueError:
        print("Entrada no válida. Por favor, ingresa un número válido.")

### GRACIAS

Hasta aquí llega el proyecto. Se espera que de cara a futuro se pueda aplicar sobre algún entorno virtual colectivo, así como implementarle nuevos juegos.
