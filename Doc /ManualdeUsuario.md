# Manual de usuario: Sistema de parqueadero

## Descripción
El sistema de gestión de parqueadero Alma Máter, es una aplicación desarrollada en Python que permite gestionar de manera eficiente las operaciones diarias del parqueadero como: registrar usuarios, controlar el ingreso 
y salida de vehículos, calcular tarifas, generar recibos y facturas, y generar reportes administrativos. 

## Requisitos del sistema
Software necesario:
Python 3.6 o superior
Sistema operativo: Windows, MacOS, o linux 
Memoria RAM: mínimo 512 MB
Espacio Disco: 50 MB libres 

## Librerías requeridas 

datetime - Para manejo de fechas y horas

csv - Para exportación de datos

os - Para operaciones del sistema

## Instalación 
1. Visita python.org
2. Descargar python 3.8 o superior 
3. Ejecuta el instalador y marca "Add python to path"
## Descarga el sistema
1. Descargar el archivo del programa main.py desde el repositorio 
2. Guardalo en una carpeta de tu elección (ej: C:\ParqueaderoAlmaMater\)
## Verificar instalación 
python --version
Debe mostrar la versión de python instalada
Inicio del sistema
1. Ejecutar el programa 
Navegar a la carpeta del programa
cd C:\ParqueaderoAlmaMater\
Ejecutar el sistema
python main.py
2. Pantalla de inicio
Al iniciar verás el menú principal:


=================================
  
        PARQUEADERO ALMA MATER
         Sistema de Gestión
    
=================================

1. Registrar Usuario
2. Ingresar Vehículo
3. Retirar Vehículo
4. Administrador
5. Salir
   
=================================


## Funcionalidades del sistema 
### 1. Registrar usuario: Permite registrar nuevos usuarios en el sistema con la sisguientes validaciones y se debe usar antes de que un cliente use el parqueadero por primera vez. 
*Datos requeridos*
-*Nombre*: Mínimo 3 letras, solo caracteres alfabéticos 
-*Apellido*: Mínimo 3 letras, solo caracteres alfabéticos
-*Documentos*: Entre 3 y 15 dígitos, solo números 
-*Placa*: Exactamente 6 caracteres (3 letras mas (+) 3 números)

*Ejemplo*
Nombre: Juan
Apellido: Pérez
Documento: 12345678
Placa: ABC123

*Errores comunes*
-*Nombre o apellidos con menos de 3 caracteres*
-*Nombres con números o caracteres especiales: "Juan123"*
-*Documentos con letras o fuera del rango permitido: "123abc"*
-*Placa con formato incorrecto: "AB1234" o "ABC12"*
Los datos correctos se registran exitosamente 

### 2. Ingresar vehículo
Se usa cuando un cliente registrado ingresa al parqueadero
*Pasos:*
1. Seleccionar la opción "Ingresar vehículo"
2. El sistema validará que el usuario esté registrado, que el vehículo no esté ya dentro, y que hayan espacios disponibles. 
3. Se registrará la hora de ingreso automáticamente 
4. Se generará un recibo en pantalla con la información del ingreso. 
*Nota:* Solo pueden ingresar vehículos de usuarios previamente registrados.
*Recibo de ingreso:*


======================================

         RECIBO DE INGRESO
      PARQUEADERO ALMA MATER
      
======================================

Nombre: Juan Pérez

Documento: 12345678

Placa: ABC123

Hora de ingreso: 2024-06-20 08:30:00

Espacios disponibles: 63

======================================

Conserve este recibo para el retiro

======================================

### 3. Retirar Vehículo
Procesa la salida de un vehículo del parqueadero y calcula el costo el parqueo 
*Sistema de tarifas*
Hora completa: $7,000 pesos
Cuarto de hora: $1,500 pesos
Pago mínimo: $7,000 pesos (equivalente a 1 hora)
*Cálculo de tarifa*
- Se calcula el tiempo total de permanencia
- Se cobra por horas completas + cuartos de hora adicionales
- Si el total es menor a $7,000, se cobra el mínimo 
*Ejemplo de cálculo:*
Tiempo: 1 hora y 37 minutos 
Horas completas: 1 × $7,000 = $7,000
Cuartos de hora: 3 × $1,500 = $4,500
**Total**: $11,500

  
============================================

            FACTURA DE PAGO
        PARQUEADERO ALMA MATER
        
=============================================

Nombre: Juan Pérez

Documento: 12345678

Placa: ABC123

Hora ingreso: 2024-06-20 08:30:00

Hora salida: 2024-06-20 10:07:00

Tiempo total: 97 minutos

---------------------------------------------

DETALLE DE COBRO:

Horas completas: 1 x $7,000 = $7,000

Cuartos de hora: 3 x $1,500 = $4,500

---------------------------------------------

TOTAL A PAGAR: $11,500

=============================================

### 4. Módulo Admnistrador
únicamente puede acceder personal autorizado con credenciales 
*credenciales de acceso:*
Usuario: admin / Contraseña: 123456
Usuario: gerente / Contraseña: almamater2024

### 5. Reportes disponibles
- Total de vehículos registrados: muestra cuantos usuarios están registrados en el sistema 
- Total de vehículos retirados: muestra cuantos vehículos han completado su estadía
- Total de vehículos sin retirar: lista los vehículos que actualmente están en el parqueadero 
  Total de vehículos sin retirar: 2
  Vehículos actualmente en el parqueadero:
  - ABC123 | Juan Pérez | 45 min
  - XYZ789 | María García | 120 min
- Total pagos de vehículos retirados
  Total de pagos recibidos: $45,500
  Número de transacciones: 6
  Pago promedio por vehículo: $7,583
- Tiempo promedio de estancia: 2 horas y 15 minutos (135.0 minutos en total)
- Lista completa de usuarios: Muestra todos los usuarios registrados con sus datos
- Vehículo con tiempo máximo y mínimo: 
  VEHÍCULO CON MAYOR TIEMPO DE PARQUEO:
  Placa: DEF456
  Propietario: Carlos López
  Tiempo: 480 minutos
  VEHÍCULO CON MENOR TIEMPO DE PARQUEO:
  Placa: GHI789
  Propietario: Ana Torres
  Tiempo: 25 minutos
- Exportar datos: 
  Genera tres archivos:
  usuarios_registrados.csv
  vehiculos_retirados.csv
  vehiculos_actuales.csv
  
### Solución de problemas
### Errores de validación
*Problema:* "Error en formato de placa"
*Solución:* Verificar que la placa tenga exactamente 3 letras, seguidas de 3 números (ejemplo: ABC123)
*Problema:* "Nombre demasiado corto"
*Solución:* Ingresar nombres y apellidos con mínimo 3 carateres 
*Problema:* "Documento inválido"
*Solución:* Usar sólo números, entre 3 y 15 dígitos 
### Errores de operación 
*Problema:* "Usuario no registrado"
*Solución:* Registrar el usuario antes de intentar ingresar el vehículo
*Problema:* "Vehículo no encontrado"
*Solución:* Verificar que la placa este escrita correctamente y que el vehículo haya ingresado 
*Problema:* "Este vehículo ya se encuentra en el parqueadero"
*Solución:* Verifica la placa o retira el vehículo
*Problema:* "No hay espacios disponibles"
*Solución:* Esperar a que salgan vehículos o revisarel reporte de vehículos actuales
###Errores de acceso
*Problema:* "Credenciales incorrectas"
*Solución:* Verificar que este utilizando:
- admin/123456 o gerente/almamater2024
*Problema: "No se crean archivos CSV
*Solución:* - Ejecutar como administrador
- Verificar los permisos de escritura
- Los archivos se crean en la misma carpeta del programa 
## Mejores prácticas 
### Para operadores: 
- Siempre registrar usuarios antes del primer ingreso
- Verificar los datos antes de confirmar registros
- Conservar los recibos hasat el retiro del vehículo
- Hacer respaldos regulares exportando a CSV
### Para administradores: 
- Revisar resportes diariamente para detectar anomalías
- Exportar datos semanalmente como respaldo
- Mantener las credenciales seguras 
- Capacitar al personal en el uso del sistema
## Capacidad y limitaciones
### Capacidades:
- 64 vehículos simultáneos 
- Usuarios ilimitados registrados 
- Historial completo de transacciones 
- Cálculo automático de tarifas 
- Reportes en tiempo real 
### Limitaciones: 
- Solo para automóviles (no motos)
- No guarda datos entre sesiones (usa CSV para respaldo)
- No maneja múltiples turnos sumultáneos 
- No tiene interfaz gráfica
## Contacto y soporte
### Soporte técnico:
- Universidad: Universidad de Antioquia
- Facultad: Facultad de ingeniería 
- Curso: Algoritmia y programación
### Equipo de desarrollo:
- Líder del proyecto: Aida Andrea Arredondo Silva 
- Desarrollador 1: Natalia Restrepo Calvo
- Desarrollador 2: Dania Paola López Torres
### Repositorio del proyecto:
- Versión: 1.0.0
- Última actualización: -----
