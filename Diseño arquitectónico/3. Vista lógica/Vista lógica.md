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

## [Enlace al diccionario de clases](https://utpl-my.sharepoint.com/:x:/g/personal/hlchuquimarca_utpl_edu_ec/Ef4Q6vqcT6ZIkBWhR8b88AsBFVgr6-DH5vroV6cvmuYZhQ?e=caQLEj)

## Foto del diagrama

<p align="center">
  <img src="https://i.postimg.cc/vHw4YfG2/Inventario-de-Bodega-Diagrama-de-clases.png" alt="Diagrama de clases"/>
</p>

---

# Diagramas de Robustez  

## ¿Qué son los diagramas de robustez?  
Los diagramas de robustez son una herramienta de modelado utilizada en el diseño de software para detallar cómo los actores, objetos, y procesos interactúan dentro de un sistema. Sirven como un puente entre los diagramas de casos de uso y los diagramas de diseño detallado, permitiendo identificar elementos clave del sistema como actores, controladores y entidades.  

## Estructura que siguen los diagramas de robustez  

- *Actores:* Representan los usuarios u otros sistemas que interactúan con el sistema principal. Se dibujan como figuras humanas o íconos.  
- *Entidades:* Son los elementos de datos o conceptos principales del dominio, representados como rectángulos.  
- *Controladores:* Representan la lógica de la aplicación y la interacción entre actores y entidades. Se muestran como círculos u óvalos.  
- *Relaciones:* Representan las conexiones entre actores, controladores y entidades mediante líneas con etiquetas que describen la interacción.

## Foto del diagrama

