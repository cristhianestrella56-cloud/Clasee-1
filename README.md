# Clasee-1

class Estudiante:
    """
    Clase estudiante que permite crear objetos de tipo estudiante.
    """

    def __init__(self, nombre, cedula, semestre, email):
        self.__nombre = nombre
        self.__cedula = cedula
        self.__semestre = semestre
        self.__email = email
        self.__materias = []  

    # GETTERS
    @property
    def nombre(self):
        return self.__nombre

    @property
    def cedula(self):
        return self.__cedula

    @property
    def semestre(self):
        return self.__semestre

    @property
    def email(self):
        return self.__email

    @property
    def materias(self):
        return self.__materias

    # SETTERS
    @nombre.setter
    def nombre(self, nuevo_nombre):
        self.__nombre = nuevo_nombre

    @cedula.setter
    def cedula(self, nueva_cedula):
        self.__cedula = nueva_cedula

    @semestre.setter
    def semestre(self, nuevo_semestre):
        self.__semestre = nuevo_semestre

    @email.setter
    def email(self, nuevo_email):
        self.__email = nuevo_email

  
    def agregar_materia(self, materia):
        self.__materias.append(materia)

    def eliminar_materia(self, materia):
        if materia in self.__materias:
            self.__materias.remove(materia)

    def __str__(self):
        return f'Estudiante [nombre: {self.__nombre}, cedula: {self.__cedula}, semestre: {self.__semestre}, email: {self.__email}, materias: {self.__materias}]'


if __name__ == '__main__':
    estudiante1 = Estudiante('Cristhian', '0964758293', '6to semestre', 'cristhiann@gmail.com')

  
    estudiante1.agregar_materia('Estadística')
    estudiante1.agregar_materia('Base de datos')
    estudiante1.agregar_materia('Programación')

    print(estudiante1)

    print(estudiante1.materias
