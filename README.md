# SOSA_LUIS_OMAR_1217_3-W_19_NOVIEMBRE
Practicas del 19 de noviembre
# PROGRAMA 1: 
class Estudiante():
    def __init__(self, nombre, edad, escuela, nota):
        self.nombre = nombre
        self.edad = edad
        self.escuela = escuela
        self.nota = nota

    def imprimir(self):
        print(f"Nombre: {self.nombre} \nEdad: {self.edad} años \nEscuela: {self.escuela} \nNota: {self.nota}")

    def resultados(self):
        if self.nota >= 7:
            print("¡Has APROBADO!")
        else:
            print("¡Has REPROBADO!")

estudiante = Estudiante("Sosa Luis Omar", 18, "CBTis 128", 9) 
estudiante.imprimir()
estudiante.resultados()

![image](https://github.com/user-attachments/assets/2630a869-a25b-46f8-9265-76ab8a7fab3a)
![image](https://github.com/user-attachments/assets/93fad5f9-a38d-4932-8198-19a0016d680d)

# PROGRAMA 2:
class Persona:
    def __init__(self, n, e):
        self.nombre = n
        self.edad = e

    def cumpleaños(self):
        self.edad += 1

# Crear la instancia de Persona con los datos proporcionados
p = Persona(input("Ingrese nombre: "), int(input("Ingrese edad: ")))

# Llamar al método cumpleaños dos veces
p.cumpleaños()
p.cumpleaños()
print(f"{p.nombre} cumple {p.edad} años")

![image](https://github.com/user-attachments/assets/b8d85b4d-1b18-4972-94bc-1c54456894f4)
![image](https://github.com/user-attachments/assets/8f8437ed-dfe2-46b7-ad79-14888611197f)

# PROGRAMA 3:
class BandaRock:
    def __init__(self, nombre_banda, num_integrantes):
        self._nombre_banda = nombre_banda
        self._num_integrantes = num_integrantes

    def agregar_integrante(self):
        self._num_integrantes += 1
        print(f"¡Un nuevo integrante se unió a {self._nombre_banda}! Ahora somos {self._num_integrantes}.")

    def quitar_integrante(self):
        if self._num_integrantes > 0:
            self._num_integrantes -= 1
            print(f"Un integrante dejó la banda {self._nombre_banda}. Ahora somos {self._num_integrantes}.")
        else:
            print(f"{self._nombre_banda} no tiene integrantes para quitar.")

    def dividir_recaudacion(self, total_recaudado):
        recaudacion_por_integrante = total_recaudado / self._num_integrantes
        print(f"Cada integrante de {self._nombre_banda} recibirá {recaudacion_por_integrante:.2f} por la recaudación.")

    def agregar_concierto(self, num_conciertos):
        print(f"{self._nombre_banda} tiene ahora {num_conciertos} conciertos programados.")

# Crear una instancia de la banda
banda = BandaRock("The Rockers", 4)

# Operaciones en la banda
banda.agregar_integrante()
banda.quitar_integrante() 
banda.dividir_recaudacion(10000)
banda.agregar_concierto(5) 

![image](https://github.com/user-attachments/assets/f17231f3-67e0-4e42-9d30-bcf148704920)
![image](https://github.com/user-attachments/assets/9dded26d-9d0d-415c-952f-d38b1df9f869)
