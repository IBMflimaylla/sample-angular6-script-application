1.	Tener instalado el angular CLI, si no lo tienes instalado
	sudo npm install -g @angular/cli

2.	Crear una aplicación nueva
    ng new demo-angular6

3.	Ingresar a la ruta
    cd ./demo-angular6

4.	Levantar la aplicación (localhost:4200)
    ng serve

5.	Compilar para producción
    ng build –buildOptimizer –aot
Genera archivos en la carpeta /dist
https://github.com/angular/angular-cli/issues/9016

En este caso debemos usar buildOptimizer porque sino el archivo vendor.js es muy grande y no se puede subir a WCM, un archivo JS solo puede pesar máximo 2MB
https://developer.ibm.com/answers/questions/365041/error-nt6577e%20-the-value-for-the-binary-property-ib.html%29/

6.	Agregar el data-scriptportlet-combine-urls="true" al index.html de la aplicación
https://github.com/OpenNTF/Script-Portlet-Node-Samples/blob/master/samples/angular_contacts/index.html

Habilitar trazas en WebSphere Portal para WCM
http://www-01.ibm.com/support/docview.wss?uid=swg21673017


7.	Configurar el ambiente WebSphere Portal

Resource environment provider -> WCM WCMConfigService, crear estas dos propiedades
dynamic.parameter.tag.enabled
renderingplugin.shortform.enabled
ambas con valor false

8.	Configurar command push line
https://developer.ibm.com/answers/questions/365041/error-nt6577e%20-the-value-for-the-binary-property-ib.html%29/

9.	Establecerse dentro de la carpeta /dist del proyecto de angular
Ejecutar el comando sp push -wcmContentName “Angular 6 Demo”
https://developer.ibm.com/answers/questions/365041/error-nt6577e%20-the-value-for-the-binary-property-ib.html%29/

10.	Crear una página en WebSphere Portal y establecer permisos
11.	Agregar a la página un Visor de Contenido Web
12.	Asociar el script portlet al visor de contenido web

13.	Ingresar a la página.
