# Proyecto_Integrador
Hagan ramas distintas para que elabore sus codigos y cuando sientan que ya quedo, hagan el branch a la rama main asi evitamos errores y mantenemos un orden.

Cada commit debe de tener un mensaje que indique cual fue la actualizacion y que errores no pudieron resolver (La idea es que no haya errores).


Aca pego una lista de los avances y los faltantes:
 
1 Presentación de la empresa (Terminado aunque se puede mejorar muchas cosas mas)

2 servicios o producto (Pendiente por hacer)

3 formulario con una tabla (crud = create, read, update, delete) (Pendiente por hacer)

4 Pega modelo entidad relación y poner cualquier código ( se puede colocar en la etiqueta "code") (Pendiente)

5 Pegar cualquier ejercicio de lógica de programación (explicar porque es el ejercicio en esa misma pagina) (Pendiente)

6 Pagina de contactos (Terminado)

7 Presentación de los integrantes (tipo fichero, se puede montar una foto cual sea) (Terminado).

Nota: Todas las paginas debe tener el mismo footer, header, head, body.

Se entrega para la semana 17 junto con el curso de GitHub.

Si quieren hacer algun cambios a su gusto son libres de hacerlo.

# Biblioteca_El_Saber


package biblioteca;

import java.util.Scanner;

public class biblioteca {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int opciondeMenuPrincipal = 0;
        int menuAdmin = 0;
        int crudCliente = 0;
        int crudServicios = 0;
        int menuCliente = 0;
        int cliente = 0;
        int maximClientes = 1000; // aqui estoy diciendo que la capacidad maxima de clientes a registrar es 1000
        String [] nombres = new String[maximClientes];
        String [] apellidos = new String[maximClientes];
        long [] cedulas = new long[maximClientes];
        long [] telefonos = new long[maximClientes];


     // mensaje de bienvenida a la libreria y opcion de que usuario ingresara.
      while (opciondeMenuPrincipal !=2 ){

          System.out.println(" BIENVENIDOS A LA LIBRERIA EL SABER");
          System.out.println(" ----------------------------------\n");
          System.out.println("¿Quien va a ingresar?\n");
          System.out.println("""
                1. Administrador.
                2. Cliente.
                """);

          opciondeMenuPrincipal = sc.nextInt();

          switch (opciondeMenuPrincipal){
              case 1:
                  menuAdmin = 0;

                  while (menuAdmin !=3){
                      System.out.println("""
                              Bienvenido Sr@. Administrador. ¿que desea realizar hoy?
                              
                              1. CRUD Clientes.
                              2. CRUD Servicios.
                              3. Volver al Menú Principal.
                              """);
                      menuAdmin = sc.nextInt();

                      switch (menuAdmin){
                          case 1:
                              crudCliente = 0;

                              while (crudCliente !=5){
                                  System.out.println("""
                                          ¿Que desea realizar?
                                          
                                          1. Agregar Cliente.
                                          2. Buscar Cliente.
                                          3. Eliminar Cliente.
                                          4. Modificar Cliente.
                                          5. volver.
                                          """);
                                  crudCliente = sc.nextInt();

                                  switch (crudCliente){
                                      case 1: //Agregar a un cliente
                                          sc.nextLine();
                                          System.out.println("Ingrese el nombre del cliente: ");
                                          nombres[cliente] = sc.nextLine();
                                          System.out.println("Ingrese el Apellido del cliente: ");
                                          apellidos [cliente] = sc.nextLine();
                                          System.out.println("Ingrese la Cedula del cliente :");
                                          cedulas [cliente] = sc.nextLong();
                                          System.out.println("Ingrese el numero telefonico del cliente: ");
                                          telefonos [cliente] = sc.nextLong();

                                          cliente++;

                                          System.out.println("Ha sido registrado Éxitosamente.");
                                          break;

                                      case 2: // Buscar a un cliente
                                          sc.nextLine();
                                          System.out.println("Ingrese el nombre del cliente que desea buscar: ");

                                          for ( int i = 0; i < cliente; i++){
                                              if (nombres [i].equals(nombres[i])){

                                                  System.out.println("CLIENTE ENCONTRADO\n");
                                                  System.out.println("Nombre: " + nombres[i]);
                                                  System.out.println("Apellidos: " + apellidos[i]);
                                                  System.out.println("Cedula: " + cedulas[i]);
                                                  System.out.println("Telefono: " + telefonos[i]);
                                                  break;
                                              } else {
                                                  System.out.println("Cliente no encontrado.");
                                              }
                                          }
                                      case 3:

                                  }
                              }

                      }
                  }

          }

      }

