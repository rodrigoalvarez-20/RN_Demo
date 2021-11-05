# Guia de instalación

Una guia simple y bonita de instalación de requerimientos de React Native en los distintos sistemas operativos

## Windows

- Instalar [Python 2.7](https://www.python.orgftppython2.7.18python-2.7.18.amd64.msi)

- Instalar [Java JDK 8](httpswww.oracle.commxjavatechnologiesjavasejavase8-archive-downloads.html)

- Instalar [NodeJS](httpsnodejs.orgdistv16.13.0node-v16.13.0-x64.msi)

## Mac OS y Linux

- Se debe de instalar NodeJS en el sistema.
- Se debe de instalar Java JDK 8 en el sistema (puede ocupar el mismo link que para windows, solo considere su plataforma de destino)
- En caso de complicacion para Linux de instalar el JDK, por favor busque instrucciones especificas
- Podemos instalar un gestor de versiones de Node, ya que es mas facil trabajar de esta manera
- Basta con ejecutar la siguiente instruccion en la terminal

`curl -o- https://raw.githubusercontent.comnvm-shnvmv0.37.2install.sh | bash`

Una vez instalado, podemos probar que se haya instalado mediante

`nvm -v`

Si no hay salida, basta con ejecutar `source ~/.zshrc` para poder recargar el archivo de la terminal

Teniendo instalado NVM, podemos instalar cualquier version de Node, basta con ejecutar `nvm install {version}`. Para este tutorial, ocuparemos la version 12 `nvm install 12`

Podremos verificar que se haya instalado de manera adecuada ejecutando `node -v` y si vemos salida, podemos continuar

Adicionalmente se debe de tener instalado Watchman para MacOs

`brew install watchman`

Y si desean, pueden ocupar el OpenJDK para Mac

`brew install --cask adoptopenjdkopenjdkadoptopenjdk8`

## Dependencias generales y consideraciones

- NodeJS
- JDK8 u OpenJDK8
- Expo-cli o react-native-cli
- Android Studio
- Android Build Tools
- Android JDK
- Si desea compilar a IOS, es necesario contar con XCode (una Mac, pa pronto)

## Trabajando con React Native

Una vez teniendo NodeJS instalado, ejecutamos el comando

`npm install -g react-native-cli`

Y esperamos a que termine de instalarse la CLI de manera global

Nota Tambien se puede trabajar con EXPO. Basta con sustituir react-native-cli por expo-cli y ocupar expo en la linea de comandos

Una vez teniendo instalado de manera global la utilidad, podemos pasar a crear nuestro proyecto.

Buscamos la carpeta en donde queremos crear nuestro proyecto y ejecutamos

`npx react-native init {nombre_del_proyecto}`

Se creara una nueva carpeta con el nombre especificado y con todos los recursos necesarios dentro.

Nos movemos al directorio y ejecutamos en terminal el comando

`npx react-native start`

Esto hace que se generen los archivos estaticos y se haga la compilacion cruzada a ambos dispositivos

La terminal se va a quedar ocupada, por lo que debemos de abrir una nueva terminal, ir a la carpeta del proyecto y ejecutar

`npx react-native run-android`

Para poder ejecutar en android, ya sea en el simulador o en un dispositivo fisico
