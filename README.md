# proyecto-final
from lifestore_file import lifestore_products
from lifestore_file import lifestore_sales
from lifestore_file import lifestore_searches

#INGRESAR UN USUARIO, PASSWORD
registro_usuarios = []
registro_password= []
desea_registrar = input("¿Desea crear una cuenta? (Ya tengo una cuenta/Registrarme: ")

#Con este while se agrega el nuevo usuario y password a la lista
while desea_registrar == "Registrarme":
  nuevo_usuario = input("Ingresa un nombre de usuario: ")
  registro_usuarios.append(nuevo_usuario)
  nueva_contraseña = input("Ingresa una contraseña: ")
  registro_password.append(nueva_contraseña)
  break
print(registro_usuarios, registro_password)

#Con este while no es necesario registrarse
while desea_registrar in "Ya tengo una cuenta": 
  usuario_existente = input("Ingresa el usuario: ")
  contraseña_existente = input("Ingresa la contraseña: ")
  break 
print("Hola, bienvenido a lifestore")

 

usuario = registro_usuarios
password = registro_password


#Con este if estamos verificando que el usuario y la contraseña esten en las listas correspondientes:
if usuario in registro_usuarios and password in registro_password: 
  print ("Hola, bienvenido a lifestore")
else:
  print ("Lo sentimos, el usuario o contraseña son incorrectos")



#MENU ¿Cómo hago que solo se presente a los usuarios?

#Con este if, le doy la permiso solo a mis usuarios de entrar
if usuario == registro_usuarios:
  print("Elige una opción: \n Opción a: Productos más vendidos y categorias con mayores busquedas \n Opción b: Productos menos vendidos y categorias con menores busquedas")
  opcion_seleccionar = input("Opción: ")
  
  #Con este while,si es diferente de a o b, presenta una opcion incorrecta 
  while opcion_seleccionar != "a" or "b":
    
    #Con este if, selecciona que desea hacer de las dos opcines del menu
    if opcion_seleccionar == "a":

      print ("Seleccionaste la opción de Productos más vendidos  y categorías con más busquedas")

      break

    elif opcion_seleccionar == "b":
      print ("Seleccionaste la opcion de Productos menos vendidos y categorias con menos busquedas") 

      break
    
    
    if opcion_seleccionar != "a" or "b":
      print ("Esta opción no existe")
    opcion_seleccionar = input("Selecciona otra opción: ")

""""

#Opcion a. Productos mas vendidos y categorias con mayores busquedas

contador = 0
total_vtas = []

for producto in lifestore_products:
  for venta in lifestore_sales:
    if producto [0] == venta[1]:
      contador = contador+ 1
   
  lista_id_vta = [producto [0], producto [1], contador]
  total_vtas.append (lista_id_vta)
  contador = 0

for total in total_vtas:
  print("el producto: ", total [1], "se vendió", total [2],"veces")


for indice in range (0,50):
  print("Nombre del producto: \n" , total_vtas[indice][1], "\n")


total_vtas.sort(key=total_vtas)
  while total_vtas:
    minimo = total_vtas [1][2]
    lista_actual = total_vtas [1]
    for total in total_vtas:
       if total_vtas[1] < minimo:
         minimo = total_vtas [1]
         lista_actual = total_vtas
        lista_ordenada.append(lista_actual)
        total_vtas.remove(lista_actual)
print(lista_ordenada))

"""



