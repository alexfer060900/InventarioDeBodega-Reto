<p align="right">
  <img src="../media/utpllogo.png" alt="Logo UTPL" width="150"/>
</p>


# Diagrama de casos de uso para la Aplicación de Gestión de inventario de Bodega

## ¿Qué es un diagrama de casos de uso?

Un diagrama de casos de uso es una representación gráfica empleada en el modelado de sistemas para describir las interacciones entre los actores (usuarios, sistemas externos u otros componentes) y las funcionalidades principales que ofrece un sistema. Este tipo de diagrama, basado en el estándar UML (Lenguaje Unificado de Modelado), se utiliza para documentar **qué hace el sistema** desde la perspectiva de los usuarios, sin entrar en detalles sobre **cómo se implementa**.

---

## ¿Para qué sirve un Diagrama de Casos de Uso?

El diagrama de casos de uso es una herramienta clave para el desarrollo y documentación de sistemas, ya que permite:

1. **Especificar requisitos funcionales**: Identificar y detallar las funcionalidades principales que debe cumplir el sistema.
2. **Facilitar la comunicación**: Servir como un medio común entre los interesados, desarrolladores y analistas para garantizar la comprensión de los requisitos.
3. **Definir el alcance del sistema**: Determinar los límites del sistema, especificando qué incluye y qué excluye.
4. **Identificar actores clave**: Describir quiénes interactuarán con el sistema, ya sean usuarios humanos o sistemas externos.
5. **Priorizar funcionalidades**: Ayudar a evaluar y clasificar las funcionalidades en función de su importancia o impacto para los usuarios.

---

## Estructura de un Diagrama de Casos de Uso

La estructura de un diagrama de casos de uso incluye los siguientes componentes principales:

1. **Actores**:
   - Representan las entidades externas que interactúan con el sistema.
   - Pueden ser personas, organizaciones o sistemas.
   - Se representan gráficamente como una figura humana o una etiqueta que los identifica.
   - Ejemplo: *Usuario*, *Administrador*, *Sistema Externo*.

2. **Casos de Uso**:
   - Representan las funcionalidades o servicios específicos que el sistema proporciona a los actores.
   - Se representan como óvalos con un nombre que describe la acción.
   - Ejemplo: *Registrar Usuario*, *Generar Informe*, *Procesar Pago*.

3. **Relaciones**:
   - **Asociación**: Representa la interacción entre un actor y un caso de uso (línea sólida).
   - **Inclusión** (`<<include>>`): Indica que un caso de uso incluye la funcionalidad de otro, generalmente para evitar redundancia.
   - **Extensión** (`<<extend>>`): Señala un caso de uso opcional que extiende la funcionalidad de otro principal, dependiendo de ciertas condiciones.
   - **Generalización**: Define relaciones de herencia entre actores o entre casos de uso.

4. **Sistema**:
   - Representa los límites del sistema modelado.
   - Se ilustra como un rectángulo que contiene los casos de uso.

---
## 1. Diagrama de caso de uso (Registro)

<p align="center">
  <img src="../media/Diagrama%20Caso%20de%20Uso%201.png" alt="Diagrama de caso de uso (Registro)"/>
</p>

   - **Ingresar usuarios**: El administrador de la aplicación ingresa usuarios al aplicativo, para validar de que ese usuario es miembro de la *Universidad técnica particular de Loja* (UTPL) y que tiene acceso a las bodegas de la universidad, extrae la información de la base de datos de la UTPL.

   - **Ingresar Componentes**: El administrador de la aplicación ingresa los componentes que posee la bodega de la UTPL, dichos componentes pueden pertenecer a una de las categorías del aplicativo, estos son, *suministros de oficina*, *equipos y mobiliario*, *tecnología*, *material deportivo*, *material de limpieza y seguridad* y *libros y material bibliográfico*.

## 2. Diagrama de caso de uso (Gestión)

<p align="center">
  <img src="../media/Diagrama%20Caso%20de%20Uso%202.png" alt="Diagrama de caso de uso (Gestion)"/>
</p>

  - **Gestionar inventario**: El personal administrativo tiene la capacidad de gestionar el inventario que posee las bodegas de la UTPL, tiene la capacidad de *clasificar componentes*, *verificar el estado del componente* en el que se encuentra en ese momento y visualizar un *historial de rotación de componentes*.

  - **Gestionar orden de compra**: El personal administrativo tiene la capacidad de gestionar la orden de compra o solicitud de componentes, para realizar dicha orden, el aplicativo *verifica la existencia de componentes* desde su base de datos interna, el personal administrativo puede *solicitar orden de compra* de los componentes que estén disponibles en el aplicativo, y por ultimo, *puede aprobar o denegar la orden compra*

## 3. Diagrama de caso de uso (Monitoreo)

<p align="center">
  <img src="../media/Diagrama%20Caso%20de%20Uso%203.png" alt="Diagrama de caso de uso (Monitoreo)"/>
</p>

- **Monitorear inventario**: El personal administrativo puede monitorear el inventario desde el aplicativo, dicho monitoreo se lo realiza *identificando el componente* y accediendo a su información, además el aplicativo tiene la capacidad de *generar un informe* que posee la información sobre el componente identificado.

- **Generar Alertas**: El aplicativo tiene la capacidad de *generar alertas en tiempo real*, estas alertas pueden ser de dos tipos, "caducidad de componentes" que es cuando un componente este próximo a caducarse, y *estado de componente* que es el estado actual del componente.

## 4. Diagrama de caso de uso (Ejecución)

<p align="center">
  <img src="../media/Diagrama%20Caso%20de%20Uso%204.png" alt="Diagrama de caso de uso (Ejecucion)"/>
</p>

- **Entregar componentes**: El personal administrativo tiene la capacidad de entregar componentes, para entregar los componentes, debe *recibir una solicitud* de componentes mediante otro aplicativo, mediante el aplicativo de gestión de inventario *despacha los componentes*, una vez recibido los componentes se *confirma la recepción* de los componentes, mediante el aplicativo de gestión de inventario se *devuelven los componentes* que ya no se desea usar.
