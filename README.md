# VueTrack
Un habit tracker hecho con Vue.

## Requisitos Funcionales
Estos son los requisitos que describen las funciones específicas **que la aplicación debe realizar**. Incluyen las acciones que la aplicación debe permitir a los usuarios realizar y cómo debe responder la aplicación a estas acciones.

Los requisitos funcionales de mi aplicaión son:
- Permitir a los usuarios crear hábitos para que puedan *trackearlos*.
- Permitir a los usuarios disponer de una sesión para poder guardar todos sus hábitos y *trackearlos* a través de varios dispositivos.
- Varias vistas de un mismo hábito (a lo commits, rachas, etc.)
- Permite al usuario tener un grupo de hábitos marcados como "Importantes". A veces uno tiene un grupo de hábitos que son más primordiales que otros pero también quiere conserver los otros. Con este grupo, el usuario se asegura que está cumpliendo si o si los más importantes y no se preocupa por no estar completando todos los hábitos que se ha propuesto (yo soy un ejemplo de esto)

## Requisitos No funcionales
Estos son los requisitos que describen las características y restricciones adicionales de la aplicación que no están relacionadas directamente con sus funciones específicas, pero que son igualmente importantes para su éxito.

Los requisitos no funcionales de mi aplicación son:
- Moderna UI.
- Aplicación muy minimalista y fácil de usar.
- Datos totalmente encriptados para asegurar la total privacidad del usuario.
- Funciona en Web, Android, iOS y PCs (Windows, MacOs y Linux)

## Requisitos de Usuario
Estos son los requisitos que se derivan de las necesidades y expectativas de los usuarios finales de la aplicación. Es importante comprender las metas y los flujos de trabajo de los usuarios para diseñar una aplicación que satisfaga sus necesidades de manera efectiva.

Los requisitos de usuario de mi aplicación son:
- Disponible en Ingles, Portuges y Español (España)
- Los hábitos serán totalmente personalizables. ¿Qué se podrá personalizar?
    - Icono hábito.
    - Color.
    - Vista.

## Vistas de la aplicación

### Vista principal

En la vista principal existirán los siguientes elementos:
- **Vista de calendario.** Permite al usuario ver el dia actual con un color de fondo dependiendo de cuantos hábitos haya completado (con un gradient a lo Apple Music)

El gradient al que me refiero:
![Ejemplo de Gradient a lo Apple Music](image.png)

- **Acciones**. Aqui se mostrarán algunas de las acciones básicas que puede hacer el usuario en la aplicación. Algunas de esas acciones son:
    - Crear un nuevo hábito.
    - Ver los hábitos más importantes.

Más abajo en esta sección están los botones casuales:
- Ajustes.
- Configuración del perfil de usuario.

### Vista "más importantes"

En esta vista, existirán un grupo de hábitos que el usuario quiera aislar de los demás para asegurarse de que los está cumpliendo si o si y dar la sensación de que está avanzando sin tener que preocuparse de llenar también los checkboxes de los demás.

En mi opinión, sentimos que estamos haciendo un mayor progreso si estamos llenando 5/7 que si 5/20.

Es por esta misma razón que existe está sección, para tener una vista que permita ver el progreso más importante que quiera el usuario realizar.

Hacerlo tipo "Caja secreta"

### Vista de Calendario

En la vista de Calendario, se abrirá un Calendario a lo aplicación de calendario, pero cada dia tendrá los colores de los hábitos para ver el progreso realizado por el usuario de una manera mucho más general.

En este vista se podrá ajustar a:
- Semana.
- Mes.
- Año.

### Tipos de vistas

Existirán diferentes tipos de vistas para que se pueda visualizar el progreso:
- Commits. (Checkboxes)
- Analytics. (Gráfico)
- Rechas

Entre otras más...