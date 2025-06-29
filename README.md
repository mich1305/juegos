print(
    "¿Qué tanto me conoces?\nEste programa está creado con el fin de saber si me conoces lo suficiente.\n"
    "Habrán 10 preguntas, en donde cada una vale 1 punto.\n"
    "Si sacas más de 6 entonces apruebas el test, de lo contrario no me podrás escribir otra vez :)"

  
)

puntos = 0

respuestas_correctas = {
    1: ["mapache"],
    2: ["pupi"],
    3: ["piratas del caribe", "piratasdelcaribe"],
    4: ["bistec de atún", "bistec de atun"],
    5: ["michelle"],
    6: ["hamburguesa"],
    7: ["helado"],
    8: ["cocacola", "coca cola"],
    9: ["serie"],
    10: ["tulipanes"]
}

# Diccionario para mostrar la forma "bonita" de la respuesta correcta
respuestas_mostrar = {
    1: "Mapache",
    2: "Pupi",
    3: "Piratas del Caribe",
    4: "Bistec de atún",
    5: "Michelle",
    6: "Hamburguesa",
    7: "Helado",
    8: "CocaCola",
    9: "Serie",
    10: "Tulipanes"
}

# Lista de preguntas
preguntas = [
    "1. ¿Cuál es mi animal favorito?: ", "2. ¿Cuál es el apodo de Violett?: ",
    "3. ¿Cuál es mi Saga favorita?: ", "4. ¿Cuál es mi comida favorita?: ",
    "5. Mi segundo nombre: ",
    "--> Las siguientes preguntas serán sobre qué prefiero",
    "6. ¿Pizza o Hamburguesa?: ", "7. ¿Helado o Canguil?: ",
    "8. ¿Pepsi o CocaCola?: ", "9. ¿Película o Serie?: ",
    "10. ¿Lirios o Tulipanes?: "
]

for i in range(1, 6):
  respuesta = input(preguntas[i - 1]).lower()
  if respuesta in respuestas_correctas[i]:
    puntos += 1
  else:
    print(f"Incorrecto. La respuesta correcta era: {respuestas_mostrar[i]}")

print(preguntas[5])

for i in range(6, 11):
  respuesta = input(preguntas[i]).lower()
  if respuesta in respuestas_correctas[i]:
    puntos += 1
  else:
    print(f"Incorrecto. La respuesta correcta era: {respuestas_mostrar[i]}")

if puntos >= 6:
  print(f"\nObtuviste {puntos} puntos. ¡Felicidades! ¡Seguiremos hablando!")
else:
  print(f"\nObtuviste {puntos} puntos. Fue un placer haberte conocido.")
