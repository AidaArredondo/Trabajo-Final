# Trabajo Final Algoritmia y Programación 2025-1
## Integrantes
- Aida Andrea Arredondo Silva
- Natalia Restrepo Calvo
- Dania Paola López Torres
   

## Descripción
Este proyecto consiste en el desarrollo de un programa de consola en Python para gestionar el parqueadero Alma Máter que presta servicio exclusivamente a automóviles en el sector de la Universidad de Antioquia. El software permitirá registrar usuarios, ingresar y retirar vehículos, generar cobros, facturas básicas, reportes administrativos y exportar la información a archivos CSV.

## Vínculos académicos y descripción

### Aida Arredondo

**Programa:** Ingeniería Industrial sexto, Facultad de Ingeniería

**Seccional**: Occidente

**Habilidades y Fortalezas:** Me considero una persona creativa, con buen sentido del diseño y con disposición a explorar y aprender cosas nuevas. Me gusta encontrar soluciones prácticas a los problemas y trabajar en equipo. Soy responsable, curiosa, me adapto fácilmente a los cambios y siempre busco mejorar en cada proyecto en el que participo.

**Semestre:** Sexto

### Natalia Restrepo Calvo

**Programa** Ingeniería Industrial, Facultad de Ingeniería 

**Seccional**: Urabá - Turbo

**Habilidades y Fortalezas:** Me considero una persona responsable, respetuosa y con capacidad para el trabajo en equipo. Me adapto con facilidad a nuevos entornos y aprendo fácilmente. Busco mejorar y aportar lo mejor de mí en cada actividad. 

**Semestre:** Inicié mi carrera profesional en el primer semestre de 2022. Sin embargo, actualmente continúo cursando asignaturas correspondientes al cuarto semestre, debido a que durante el año 2024 suspendí temporalmente mis estudios por motivos de maternidad.. 

### Dania Paola López Torres

**Programa** Ingeniería Industrial, Facultad de Ingeniería

**Seccional**: Norte - Yarumal

**Habilidades y Fortalezas:** Me considero una persona tranquila, empática y responsable, con capacidad de trabajar en equipo y actitud colaborativa. Busco superar cada una de mis metas personales y profesionales, manteniendo una actitud de mejora continua. 

**Semestre:** Este semestre (2025-1) finzalizo materias de tercer semestre, sin embargo también tengo de cuarto y quinto semestre. 

## Parqueadero Alma Máter 
Espacio exclusivo para el estacionamiento de automóviles de la comunidad universitaria de la Universidad de Antioquia. Actualemente, el proceso es manual y necesita un sistema en Python para gestionar usuarios, controlar entradas y salidas, generar cobros y emitir reportes. El parqueadero opera de 06:00 am a 12:00 pm con tres empleados en turnos de 6 horas. 

![Parqueadero Alma Máter](https://github.com/AidaArredondo/Trabajo-Final/blob/7d8426452a3a4366859b99315a22bae65fe32c10/Imagen%20Parqueadero%20del%20Proyecto.png)

## Licencia de Software
La licencia recomendada para el software es **Creative Commons Atribución 4.0 Internacional** [Click para ver la licencia](https://chooser-beta.creativecommons.org/)
Esta licencia exige que los reutilizadores den crédito al creador. Permite distribuir, remezclar, adaptar y desarrollar el material en cualquier medio o formato, incluso con fines comerciales.

Con esta licencia se tiene libertad para:
Compartir: copiar y redistribuir el material en cualquier medio o formato para cualquier propósito, incluso comercial.
Adaptar: remezclar, transformar y desarrollar el material para cualquier propósito, incluso comercial.
El licenciante no puede revocar estas libertades siempre que cumpla con los términos de la licencia.
Bajo los siguientes términos:
Atribución: debe otorgar el crédito correspondiente, proporcionar un enlace a la licencia e indicar si se realizaron cambios. Puede hacerlo de cualquier manera razonable, pero no de ninguna manera que sugiera que el licenciante lo respalda a usted o a su uso.
Sin restricciones adicionales: no puede aplicar términos legales ni medidas tecnológicas que restrinjan legalmente a otros hacer lo que permite la licencia.
Avisos:
No tiene que cumplir con la licencia para elementos del material de dominio público o cuando su uso esté permitido por una excepción o limitación aplicable.

No se ofrecen garantías. Es posible que la licencia no le otorgue todos los permisos necesarios para el uso previsto. Por ejemplo, otros derechos como la publicidad, la privacidad o los derechos morales pueden limitar el modo en que utiliza el material.


## Reporte de visión: Software de gestión para el parqueadero Alma Máter
**Descripción general del software:** 

El software de gestión para el parqueadero Alma Máter será una aplicación de consola desarrollada en Python, diseñada para automatizar y optimizar las opraciones diarias del parqueadero. Su interfaz sera intuitiva y de fácil uso para el personal, permitiéndoles gestionar eficientemente el ingreso y salida de vehículos, el registro de usuarios, la generación de cobros y facturas, y la creación de reportes administrativos.

### **Objetivos:**
El objetivo principal de este software es modernizar la gestión del parqueadero, pasando de un sistema manual a uno digitalizado. Esto se logrará mediante las siguientes funcionalidades clave:

**Registros de Usuarios:** El operario registrará cada vehículo al momento de su ingreso, indicando:
-Placa del vehículo
-Fecha y hora de entrada
-Tipo de usuario: visitante o frecuente
-Espacio de parqueo asignado (si aplica)
En el caso de usuarios frecuentes, sus datos estarán previamente almacenados, lo que agiliza el proceso de ingreso.

**Gestión de ingreso y salidas de vehículos:** El sistema mostrará la disponibilidad de espacios en tiempo real, permitirá al operario asignar el espacio más adecuado según el tipo de vehículo y la disponibilidad del momento. Al momento de la salida, el sistema solicitará la placa del vehículo para:
-Verificar su registro de ingreso
-Calcular automáticamente el tiempo de permanencia
-Determinar el valor a pagar según las tarifas configuradas (por hora y fracción)

**Cálculo automático de cobros:** El sistema aplicará la tarifa establecida en el parqueadero, basada en:
-Tiempo total de permanencia
-Posibles franjas horarias con precios diferenciados (si se implementan)
Este cálculo será preciso, transparente y visible tanto para el operario como para el usuario.

**Generación de facturas:** Para quienes lo requieran, el sistema generará una factura detallada con:
-Datos del vehículo
-Tiempo de permanencia
-Valor total pagado
-Fecha y hora del servicio

**Generación de reportes administrativos:** Se producirán reportes periódicos que permitan al administrador del parqueadero tener una visión clara de la ocupación, los ingresos generados, el flujo de vehículos, y otros datos relevantes para la toma de decisiones. 

**Interfaz de consola amigable:** Desarrollar una interfaz de línea de comandos en Python que sea visualmente organizada y fácil de navegar para los operarios del parqueadero.

**Exportación de datos:** Permitir la exportación de los datos generados (registros, cobros, etc.) a un archivo plano en formato CSV para su posterior análisis o almacenamiento.

### **Beneficios:**
La implementación de este software de gestión traerá consigo una serie de beneficios significativos para el parqueadero Alma Máter, los cuales son:

**Mayor eficiencia operativa:** La automatización de tareas como el registro de ingresos y salidas, y el cálculo de cobros, reducirá el tiempo dedicado a esta actividades manuales, permitiendo al personal enfocarse en brindar un mejor servicio al cliente. 

**Reducción de errores:** Eliminar el registro manual en papel minimizará los errores humanos asociados a la transcripción de datos y al cálculo de tarifas.

**Mejor control de ingresos:** El sistema registrará de manera precisa todos los ingresos generados, facilitando la gestión financiera y la detección de posibles inconsistencias.

**Información para la toma de decisiones:** Los reportes administrativos proporcionarán datos valiosos sobre la ocupación del parqueadero, los horarios de mayor demanda, y otros indicadores clave que ayudarán a optimizar la operación y la planificación futura.

**Mejora en la expriencia del usuario:** La posibilidad de generar facturas y la agilización del proceso de pago pueden mejorar la sasisfacción de los usuarios del parqueadero.

**Profesionalización de la imagen:** La implementaciòn de un sistema digitalizado proyectará una imagen más moderna y profesional del parqueadero.

**Facilidad de seguimiento:** El registro digital de los vehículos y los usuarios facilitará el seguimiento en caso de cualquier eventualidad.

## **Gestión operativa del parqueadero:**

### **Requisitos funcionales:**
Acciones y comportamientos específicos que debe realizar el sistema del parqueadero Alma Máter. Estos incluyen:

**Gestión de usuarios:**
- Registrar nuevos usuarios con validaciones
- Nombre y apellido: mínimo tres letras, sin números.
- Documento: entre 3 y 15 caracteres, solo dígitos.
- Placa: exactamente seis caracteres (tres letras seguidas de tres números)
  
**Ingreso de vehículos:**
  - solo se permite el ingreso de vehículos registrados.
  - Registro de hora y minuto de entrada.
  - Generación de un recibo virtual al ingresar.
    
 **Retiro de vehículos:**
- Validación de que el usuario y el vehículo estén registrados.
- Cálculo del tiempo de permanencia y cobro:
-$ 7000 por hora completa
-$ 1500 por cada cuarto de hora adicional
- Mínimo a pagar $ 7000
- Generación de facturas en pantalla al salir. 
  
**Reportes administrativos (acceso restringido por usuario y contraseña)**

- Total de vehículos registrados.

- Total de vehículos retirados.

- Total de vehículos actualmente en el parqueadero.

- Total de dinero recibido por cobros.

- Tiempo promedio de permanencia por vehículo.

- Listado de usuarios registrados.

- Vehículo con mayor y menor tiempo de permanencia.

**Exportación de datos**

- Exportar los reportes y registros a un archivo plano (.CSV).
  

**Gestión del espacio del parqueo**

- Llevar el control del total de espacios disponibles (64 en total).

### **Requisitos no funcionales**

**Usabilidad:**

- Interfaz por consola clara, intutitiva y amigable.

- Mensajes de error comprensibles.

 **Rendimiento:**

 - Respuesta rápida en operaciones (registro,ingreso,retiro, consulta).
 
 - Capacidad para mejorar múltiples registros sin afectar el rendimiento.
 
 **Fiabilidad:**

 - Garantía de integridad de datos.
 
 - Validaciones constantes para evitar errores o duplicados.
 
 **Seguridad:**

 - Acceso a administración protegido con usuario y contraseña.
 
 - Validación de datos para prevenir entradas maliciosas
 
 **Compatbilidad:**

 - Compatible con entorni Phyton estándar (Windows. Linux, MacOS).
 
 - Exportación de archivos .CSV legibles en excel o Google Sheets

## Diagrama de Gantt Chart
![Diagrama de Gantt](https://github.com/AidaArredondo/Trabajo-Final/blob/1cfa53efc02746d496aec995f3d1f01a722641cd/Gantt/Diagrama%20de%20Gantt%20Final%20Completo%2008%20Julio.png)

## Presupuesto estimado del proyecto software para el parqueadero Alma Máter:

**Base del cálculo:**
A partir del 1 de enero del 2025, en Colombia aplica la reducción de la jornada laboral a 46 horas semanales, lo que da como resultado 230 horas laboradas en el mes.
Con base en el salario mínimo legal vigente (SMLV) para ese año, el valor de la hora ordinaria queda en $6.189.

![Tabla de presupuesto](https://github.com/AidaArredondo/Trabajo-Final/blob/a30da367624e689822b46f44b311d435d683960a/TABLA%20PRESUPUESTO.png)

**Sobre el proyecto:**

El trabajo será realizado por tres estudiantes, quienes estiman invertir un total de 50 horas para completar el proyecto.
Estas horas no se pagarán en dinero, sino que corresponden a tiempo de práctica formativa, valorado como si fuera tiempo de trabajo con base en el SMLV.

**Cálculo:**

50 horas * $6.189 = $309.450

Total estimado por el tiempo invertido: $309.450 COP

Este valor representa lo que costaría el tiempo invertido si se pagara como una práctica profesional, aunque no será remunerado económicamente.

## Plan de versionado del Software
El plan de versionado describe el avance del desarrollo del Software de gestión de Alma Máter, registrando cada versión y los procedimientos relevantes realizados durante la codificación y desarrollo del sistema.

## Cronograma de Versiones del Software

### **v0.1 - Estructura Inicial del Programa**

**Fecha:** 14 de mayo de 2025 (Inicio del desarrollo del programa)

**Procedimientos realizados:**
- Creación de la estructura básica del programa Python
- Implementación del menú principal
- Definición de funciones base del sistema
- Configuarción inicial de variables y estructuras de datos
  
**Estado:** Completado

### **v0.2 - Módulo de Registro de Usuarios**

**Fecha:** 18 de Mayo de 2025

**Procedimientos realizados:**
- Implementación de función de registro de usuarios
- Desarrollo de validaciones para nombre y apellido
- Implementación de validación de documento (3-15 dígitos)
- Desarrollo de validación de placa
- Sistema de manejo de errores de validación
  
**Estado:** Completado

### **v0.3 - Módulo de Ingreso de Vehículos**

**Feccha:** 22 de mayo de 2025

**Procedimientos realizados:**
- Implementación de función de ingreso de vehículos
- Validación de usuarios registrados
- Registro automático de hora de ingreso
- Generación de recio de ingreso en pantalla
- Almacenamiento de datos de vehículos ingresados
 
**Estado:** Completado

### **v0.4 - Sistema de Cálculo de Tarifas**

**Fecha:** 26 de mayo de 2025

**Procedimientos realizados:**
- Implementación de cálculo de tiempo de permanencia
- Desarrollo de algoritmo de cobro por horas ($7.000)
- Implementación de cobro por cuartos de hora ($1.500)
- Configuración de pago mínimo ($7.000)
- Sistema de cálculo de total a pagar
   
**Estado:** Completado
    
### **v0.5 - Módulo de Retiro de Vehículos**

**Fecha:** 29 de mayo de 2025

**Procedimientos realizados:**
- Implementación de función de retiro de vehículos
- Integración con sistema de cálculo de tarifas
- Validación de vehículos registrados
- Generación de factura de pago
- Actualización de estado de vehículos retirados
    
**Estado:** Completado

### **v1.0 - Módulo de Administrador**

**Fecha:** 02 de junio de 2025

**Procedimientos realizados:**
- Implementación de sistema de autenticación de administrador
- Desarrollo de reporte de total de vehículos registrados
- Implementación de reporte de vehículos retirados
- Desarrollo de cálculo de tiempo promedio de estancia
- Implementación de lista de usuarios registrados
- Desarrollo de reporte de vehículo con tiempo máximo y mínimo
    
**Estado:** Completado

## **v1.1 - Optimización y Corrección de Errores**

**Fecha:** 08 de junio de 2025

**Procedimientos realizados:**
- Corrección de errores en validaciones
- Optimización de funciones de cálculo
- Mejora en el manejo de excepciones
**Estado:** Completado

## **v1.2 - Versión Final del Software**

**Fecha:** 15 de junio de 2025

**Procedimientos realizados:**
- Pruebas finales de integración
- Validación completa de todos los módulos
  
**Estado:** Completado

## **v1.3 - Organización del repositorio**

**Fecha:** 07 de julio de 2025

**Procedimientos realizados:**
- Creación de la carpeta "src" en GitHub
- Creación de carpeta "doc" en GitHub
- Elaboración y subida del manual de usuario
- Creación del plan de versioando del Software
  
**Estado:** Completado

## **Evolución del código**

**Funcionalidades por versión**

**v0.1 - v0.2: Fundamentos del sistema**
- Estructura base del programa
- Sistema de validaciones

**v0.3 - v0.5: Core del parqueadero**
- Gestión de vehículos
- Sistema de cobros

**v1.0: Módulo administrativo**
- Reportes y estadísticas
- Gestión completa

**v1.1 - v1.2: Refinamiento**
- Corrección de errores
- Optimización de rendimiento

**v1.3: Documentación y organización**
- Estructura de repositorio
- Documentación técnica




