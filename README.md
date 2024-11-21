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

# PROGRAMA 4:
class Persona:
    def __init__(self, nom, ape):
        self.nombre = nom
        self.apellido = ape

    def nombre_completo(self):
        print(self.nombre + " " + self.apellido)

class Estudiante(Persona):
    def __init__(self, nom, ape, comida):
        super().__init__(nom, ape)
        self.comida_favorita = comida

    def mostrar_comida_favorita(self):
        print("Comida favorita:", self.comida_favorita)


persona = Estudiante("Juan", "Pérez", "Tacos al pastor")
persona.nombre_completo()
persona.mostrar_comida_favorita()

![image](https://github.com/user-attachments/assets/39c9fdf1-5ab9-489f-85a3-03dca527246e)
![image](https://github.com/user-attachments/assets/c0460c14-4875-4c45-86eb-5ccc19ac1e5b)

# PROGRAMA 5:
class Fabrica:
    def __init__(self, llantas, color, precio):
        self._llantas = llantas
        self._color = color
        self._precio = precio

    def cantidad(self):
        print("La cantidad de llantas: {}\nEl color es: {}\nEl precio es: {}".format(self._llantas, self._color, self._precio))

class Moto(Fabrica):
    pass

class Carro(Fabrica):
    pass

# Creación del objeto Moto
print("OBJETO = moto")
moto = Moto(2, "Gris", "$200")
moto.cantidad()

# Creación del objeto Carro
print("\nOBJETO = carro")
carro = Carro(4, "Negro", "$600")
carro.cantidad()

![image](https://github.com/user-attachments/assets/3f6fa3a5-1cd7-4f6c-8ed9-962a758e87b1)
![image](https://github.com/user-attachments/assets/1569bb3d-5a21-4a16-92f2-65a4135e47d2)

# PROGRAMA 6:
class Marino:
    def hablar(self):
        print("¡Hola! Soy un habitante del océano.")

class Pulpo(Marino):
    def hablar(self):
        print("¡Hola! Soy un pulpo, maestro del camuflaje.")

class Foca(Marino):
    def hablar(self, mensaje):
        self.mensaje = mensaje
        print(f"La foca dice: {mensaje}")

marino = Marino()
marino.hablar()

pulpo = Pulpo()
pulpo.hablar()  

foca = Foca()
foca.hablar("¡Hola! Soy una foca, me encanta tomar el sol en la costa.")

![image](https://github.com/user-attachments/assets/320126bc-894f-438a-b304-a2e4d80a032c)
![image](https://github.com/user-attachments/assets/79e644cc-af7e-4ea7-bf41-d003c12d63f6)

# PROGRAMA 7:
class Musica:
    def __init__(self, nombre_banda):
        self.nombre_banda = nombre_banda

class Genero:
    def asignar_genero(self, genero):
        self.genero = genero

class Cantante(Musica, Genero):
    def datos(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
        print(f"El nombre del cantante es {self.nombre}, tiene {self.edad} años, pertenece al género {self.genero}. Forma parte de la banda {self.nombre_banda}.")
        
cantante = Cantante("Queen")
cantante.asignar_genero("Rock")
cantante.datos("Freddie Mercury", 45)

![image](https://github.com/user-attachments/assets/cf8a3d60-9e2c-4b39-9dac-0126784f426a)
![image](https://github.com/user-attachments/assets/1611fdb3-e870-4ca9-95fa-8941eacc4000)
