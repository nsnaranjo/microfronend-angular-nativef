# Aplicación Microfrontends - Angular

La aplicación `app-host` y la aplicación `app-remote` están desarrolladas en  [Angular CLI](https://github.com/angular/angular-cli) versión 18.0.0. y [Native-Federation](https://www.npmjs.com/package/@angular-architects/native-federation) versión 18.0.2.

Se implementa Clean Architecture (Arquitectura Limpia) para la organización de archivos y separación de lógica en capas, lo que facilitará la mantenibilidad y escalabilidad de los proyectos a largo plazo.

La aplicación implementa la carga dinámica de componentes de la aplicación remota, se realiza una comunicación entre componentes basada en eventos implementando una librería personalizada que hace uso de diferentes métodos de la librería [RxJs](https://rxjs.dev/guide/overview) versión 7.8.0.

Este proyecto se realiza con fines de prueba y entendimiento para el desarrollo de aplicaciones basadas en microfronends.

## Instalación y Configuración de Native Federetion en Proyectos Nuevos

### Instalación

```
npm install @angular-architects/native-federation@18.0.2 -D
```

### Configuración

Estos comando realizarán y crearán una serie de archivos y configuraciones para que la aplicación host pueda acceder a los componentes compartidos desde la aplicación remote.

Para la aplicación `host`. Recuerda cambiar la palabra `shell` por el nombre de la aplicación principal de tu proyecto.

```
ng g @angular-architects/native-federation:init --project shell --port 4200 --type dynamic-host
```

Para la aplicación `remote`. Recuerda cambiar la palabra `mfe1` por el nombre de la aplicación remota o microfronend de tu proyecto.

```
ng g @angular-architects/native-federation:init --project mfe1 --port 4201 --type remote
```
