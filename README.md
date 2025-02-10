# Casos-de-uso

### **1. Crea el diagrama de uso haciendo uso de platuml, representado los actores y casos de uso que identifiques en los requisitos\.** 

### ![image](https://github.com/user-attachments/assets/dac88d83-5af3-471e-accd-900a2aef4a74)


```Plantuml
@startuml
actor Cliente
actor Banco

usecase "Validar Cliente" as UC1
usecase "Sacar Dinero" as UC2
usecase "Transferir Dinero" as UC3
usecase "Ingresar Dinero" as UC4
usecase "Avisar de Saldo Insuficiente" as UC5
usecase "Avisar de Límite Diario Superado" as UC6

Cliente -> UC1
UC1 -> UC2 : <<include>>
UC1 -> UC3 : <<include>>
UC1 -> UC4 : <<include>>
UC2 -> UC5 : <<extend>>
UC2 -> UC6 : <<extend>>
@enduml
```
### 

### 

### **2. Describe, haciendo uso de la plantilla, al menos el caso de uso "Sacar dinero", con las interacciones que tiene entre el actor y el caso de uso\.** 

Primero el cliente debe estar validado en el cajero.  
El cliente selecciona la opción "Sacar Dinero" en el menú del cajero.  
El sistema verifica que el cliente tiene saldo suficiente.  
El sistema verifica que el monto no exceda el límite diario permitido.  
El sistema entrega el dinero al cliente.  
El sistema actualiza el saldo en la cuenta del cliente.  
El sistema genera un recibo opcional.

A1: Saldo insuficiente  
El sistema detecta que el saldo de la cuenta es insuficiente.  
A2: Límite diario superado  
El sistema detecta que el monto supera el límite diario permitido.

### 

### **3. Responde a las siguiente pregunta:¿Para qué me sirve tener/realizar un diagrama de casos de uso modelando el sistema que se representa? ¿Qué aporta?\.**

Un diagrama de casos de uso permite modelar y visualizar de manera clara las funcionalidades principales del sistema, identificando las interacciones entre los actores y las acciones que realizan. Esto aporta una comunicación clara, documentación y base para análisis.
