<p align="right">
  <img src="https://i.postimg.cc/13qQdqZs/utpllogo.png" alt="Logo UTPL" width="150"/>
</p>


# Diagrama de casos de uso 

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
  <img src="https://i.postimg.cc/NFFhky4h/Inventario-de-Bodega-Caso-de-Uso-1.png" alt="Diagrama de caso de uso (Registro)"/>
</p>

## Descripción del caso del primer uso: Registro 

### Caso: Ingresar usuarios

| *Nombre*           | Ingresar Usuario|
|-----------------------|-------------------------------------------------|
| *Actores*          | - Personal administrativo<br>- BD UTPL       |
| *Flujo normal*     | 1. El personal administrativo ingresa sus credenciales a UTPL.<br>2. UTPL valida las credenciales del personal administrativo.<br>|

1. El personal administrativo ingresa sus credenciales a UTPL.
2. UTPL valida las credenciales del personal administrativo. 

### Caso: Ingresar Componentes

1. El personal administrativo ingresa un componente al inventario.
2. El inventario valida la existencia del componente.
3. El inventario guarda el componente. 

## 2. Diagrama de caso de uso (Gestión)

<p align="center">
  <img src="https://i.postimg.cc/L5bcCHCJ/Inventario-de-Bodega-Caso-de-Uso-2.png" alt="Diagrama de caso de uso (Gestion)"/>
</p>

 ## Descripción del segundo caso de uso: Gestión 

 ### Caso: Gestionar Inventario

1. Personal administrativo verifica la existencia del componente. 
2. El inventario valida la existencia del componente.  
3. Personal administrativo verifica el estado del componente. 
4. El inventario actualiza el estado del componente. 

 ### Caso: Clasificar Componentes 

1.Personal administrativo clasifica los componentes según su tipo. 
2. El inventario muestra los componentes por tipo. 

## 3. Diagrama de caso de uso (Monitoreo)

<p align="center">
  <img src="https://i.postimg.cc/9FzVGk84/Inventario-de-Bodega-Caso-de-Uso-3.png" alt="Diagrama de caso de uso (Monitoreo)"/>
</p>

 ## Descripción del tercer caso de uso: Monitoreo

 ### Caso: Generar informe del Componente 
 
1. El inventario notifica irregularidad del componente. 
2. Inventario genera informe del componente. 
3. El personal administrativo revisa el informe 

 ### Caso: Generar alertas 
 
1. El inventario detecta condiciones de alerta 
2. El inventario genera la alerta 
3. El personal administrativo recibe la alerta 

 ### Caso: Monitorear movimientos del componente 
 
1. El inventario notifica los ingresos de los componentes. 
2. El personal administrativo monitorea los ingresos de los componentes. 
3. El inventario notifica los egresos de los componentes. 
4. El personal administrativo monitorea los egresos de los componentes 

## 4. Diagrama de caso de uso (Ejecución)

<p align="center">
  <img src="https://i.postimg.cc/v80bxyzF/Inventario-de-Bodega-Caso-de-Uso-4.png" alt="Diagrama de caso de uso (Ejecucion)"/>
</p>

 ### Caso: Solicitar Componentes 
 
1. El servicio checklist del inventario envía solicitud del componente. 
2. Personal administrativo recibe solicitud del componente.  
3. Personal administrativo acepta o rechaza la solicitud del componente. 
