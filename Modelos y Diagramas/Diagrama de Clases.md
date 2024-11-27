<p align="right">
  <img src="https://i.postimg.cc/13qQdqZs/utpllogo.png" alt="Logo UTPL" width="150"/>
</p>

# Diagrama de Clases

## ¿Qué es un diagrama de clases?

Un **diagrama de clases** es un tipo de diagrama estático en la Programación Orientada a Objetos (POO) que modela la estructura de un sistema mostrando:  
1. **Clases**: Representan las entidades o conceptos del sistema.  
2. **Atributos**: Definen las características o propiedades de cada clase.  
3. **Métodos**: Especifican los comportamientos o acciones que puede realizar la clase.  
4. **Relaciones**: Muestran las conexiones entre las clases, como asociaciones, composiciones o herencias.

Es ampliamente utilizado en la fase de diseño de software para definir cómo interactúan las diferentes partes del sistema.

---

## Estructura general de un diagrama de clases

Un diagrama de clases sigue la siguiente estructura:

1. **Clases**:  
   - Representadas como rectángulos divididos en tres secciones:  
     - **Nombre** de la clase (parte superior).  
     - **Atributos** (parte media).  
     - **Métodos** (parte inferior).  

2. **Relaciones entre clases**:  
   - **Asociaciones**: Indican conexiones entre clases.  
   - **Composición**: Una clase contiene a otra como parte esencial.  
   - **Agregación**: Una clase contiene a otra, pero no de manera esencial.  
   - **Herencia**: Una clase hereda propiedades y métodos de otra.  

3. **Visibilidad de atributos y métodos**:  
   - `+` Público: Accesible desde cualquier lugar.  
   - `-` Privado: Accesible solo dentro de la clase.  
   - `#` Protegido: Accesible dentro de la clase y sus subclases.  

4. **Cardinalidad**: Define la cantidad de objetos relacionados, como `1:1`, `1:N` o `N:M`.

---

## Foto del diagrama

<p align="center">
  <img src="https://i.postimg.cc/vHw4YfG2/Inventario-de-Bodega-Diagrama-de-clases.png" alt="Diagrama de clases"/>
</p>

## [Enlace al diccionario de clases](https://utpl-my.sharepoint.com/:x:/g/personal/hlchuquimarca_utpl_edu_ec/Ef4Q6vqcT6ZIkBWhR8b88AsBFVgr6-DH5vroV6cvmuYZhQ?e=caQLEj)

---

## Explicación del diagrama

Este diagrama de clases modela un sistema de **Inventario de Bodega**. Sus componentes principales son:

### Clases Principales

- **BDUTPL**  
  - Representa la conexión con la base de datos.  
  - Métodos: Validar credenciales y obtener datos de usuarios.

- **PersonalAdministrativo**  
  - Define a los usuarios administrativos del sistema.  
  - Métodos: Verificar componentes, procesar solicitudes y monitorear movimientos.

- **Inventario**  
  - Clase central que gestiona los componentes, movimientos y alertas.  
  - Métodos: Agregar componentes, generar alertas, registrar movimientos y notificar informes.

- **Componente**  
  - Representa los elementos almacenados en el inventario.  
  - Atributos: Nombre, tipo, estado, cantidad, fecha de ingreso, entre otros.  
  - Métodos: Actualizar estado, validar existencia y generar informes.

- **Movimiento**  
  - Registra las transacciones relacionadas con componentes del inventario.  
  - Atributos: ID del movimiento, componente asociado, cantidad, fecha y responsable.

- **Alerta**  
  - Clase encargada de notificar eventos importantes en el sistema.  
  - Atributos: Tipo de alerta, mensaje y componente relacionado.

- **Informe**  
  - Genera reportes sobre irregularidades o eventos específicos en el inventario.

- **Solicitud**  
  - Maneja los pedidos de componentes del inventario.  
  - Atributos: Componente solicitado, cantidad, fecha de solicitud, estado y solicitante.

### Relaciones Principales

1. `Inventario` administra `Componentes`, `Movimientos` y genera `Alertas`.  
2. `PersonalAdministrativo` realiza acciones sobre el inventario y procesa solicitudes.  
3. `Componentes` están relacionados con `Movimientos`, `Alertas` e `Informes`.  
4. `Solicitudes` están asociadas a componentes y son gestionadas por personal administrativo.

Este diseño es un modelo claro y organizado que sigue los principios de la Programación Orientada a Objetos, facilitando la representación de un sistema de inventario de bodega.
