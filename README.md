# Instalación y Configuración de React Native con Expo

Este documento describe el proceso de instalación y configuración de un proyecto **React Native** utilizando **Expo**, incluyendo los requisitos previos, herramientas recomendadas y la solución aplicada para lograr compatibilidad con la aplicación móvil **Expo Go**.

---

## 1. Instalación de Node.js

Antes de comenzar, es necesario tener instalado **Node.js**. Si no lo tienes, puedes descargarlo desde el sitio oficial:

🔗 [Descargar Node.js](https://nodejs.org/es/download)

Una vez instalado, verifica que la instalación fue exitosa ejecutando los siguientes comandos en tu terminal:

```bash
node -v
npm -v
```

En mi entorno de desarrollo, cuento con las siguientes versiones:

```bash
C:\Users\ASUS-GAMING>node -v
v24.14.1

C:\Users\ASUS-GAMING>npm -v
11.11.0
```

---

## 2. Instalación de Git

También es fundamental contar con **Git** para el control de versiones. Puedes obtenerlo aquí:

🔗 [Descargar Git](https://git-scm.com/install/)

Para verificar la instalación, ejecuta:

```bash
git --version
```

Resultado obtenido:

```bash
C:\Users\ASUS-GAMING>git --version
git version 2.53.0.windows.2
```

---

## 3. Configuración del Entorno de Desarrollo

Para este proyecto se utilizó **Visual Studio Code**. Se recomienda instalar las siguientes extensiones para mejorar la productividad:

*   **ES7+ React/Redux snippets**: Atajos para código React.
*   **React Native Tools**: Depuración y herramientas para React Native.
*   **Prettier**: Formateador de código automático.
*   **Material Icon Theme**: Iconos visuales para carpetas y archivos.
*   **Error Lens**: Resaltado de errores directamente en la línea de código.

---

## 4. Creación del Proyecto con Expo

Anteriormente, Expo se gestionaba mediante `expo-cli` de forma global:

```bash
npm install -g expo-cli
```

Sin embargo, el estándar actual es utilizar `npx` para asegurar que siempre usamos la versión más reciente sin instalaciones globales innecesarias:

```bash
npx create-expo-app@latest
```

Para inicializar este proyecto, ejecuté el siguiente comando:

```bash
npx create-expo-app@latest ReactNativeWithExpo
```

El asistente generará automáticamente la estructura del proyecto e instalará todas las dependencias. Una vez finalizado, ingresamos al directorio:

```bash
cd ReactNativeWithExpo
```

Y arrancamos el servidor de desarrollo:

```bash
npx expo start
```

---

## 5. Inicio del Proyecto y Vinculación

Al ejecutar `npx expo start`, Expo genera un **código QR** en la consola. Este código es la llave para vincular tu entorno de desarrollo con tu dispositivo físico.

### Código QR generado por Expo
![QR generado por Expo](https://private-us-east-1.manuscdn.com/sessionFile/6VKii6jHNM5Cs1F6PPSGtt/sandbox/2pLM4qBivWGbewJUtXLCmf-images_1780469813996_na1fn_L2hvbWUvdWJ1bnR1L1JlYWN0TmF0aXZlLUV4cG8vaW1nL25weEV4cG9TdGFydA.jpg?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvNlZLaWk2akhOTTVDczFGNlBQU0d0dC9zYW5kYm94LzJwTE00cUJpdldHYmV3SlV0WExDbWYtaW1hZ2VzXzE3ODA0Njk4MTM5OTZfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwxSmxZV04wVG1GMGFYWmxMVVY0Y0c4dmFXMW5MMjV3ZUVWNGNHOVRkR0Z5ZEEuanBnIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzk4NzYxNjAwfX19XX0_&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=H61OLTsEP9PHg7M9t-lVeEPQcfiuK2nrtlUPODnl3XBDDd8UOT720JTMEVWGop7mhW4~Kyjh~RAvbsLIqn0Rz1pBp1DuGX4CtexexDBNp90Hce7bGf1X102VzfgnV7NmtpSPULVwCuCjf~DzsGAtLGJYxV8KCJ1pxrR45gUSwtwvQzIUOSRMgvs7mvmGfo7PfFaLF96O1gqS-LSU4M4RWu2WYSPQTCuoJmDHf-lNkNfOk69qNu36lENKYAluxUg0E60zfyoig1zUVkAoUrwMkbrGj4pJt53HT5LpUoToaaaJMXwlJvMTM1~SmY17edozXSJEvKciokLP63CO5LHd4Q__)

---

## 6. Instalación de Expo Go en el Dispositivo Móvil

Para visualizar la aplicación en un teléfono real (Android o iOS), es necesario instalar la app **Expo Go** desde la tienda correspondiente.

Durante la carga inicial de la aplicación en el móvil, verás una pantalla de progreso:

### Pantalla de carga de Expo Go
![Carga Expo Go](https://private-us-east-1.manuscdn.com/sessionFile/6VKii6jHNM5Cs1F6PPSGtt/sandbox/2pLM4qBivWGbewJUtXLCmf-images_1780469813996_na1fn_L2hvbWUvdWJ1bnR1L1JlYWN0TmF0aXZlLUV4cG8vaW1nL2NoYXJnZUV4cG9tb3ZpbA.jpg?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvNlZLaWk2akhOTTVDczFGNlBQU0d0dC9zYW5kYm94LzJwTE00cUJpdldHYmV3SlV0WExDbWYtaW1hZ2VzXzE3ODA0Njk4MTM5OTZfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwxSmxZV04wVG1GMGFYWmxMVVY0Y0c4dmFXMW5MMk5vWVhKblpVVjRjRzl0YjNacGJBLmpwZyIsIkNvbmRpdGlvbiI6eyJEYXRlTGVzc1RoYW4iOnsiQVdTOkVwb2NoVGltZSI6MTc5ODc2MTYwMH19fV19&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=LZaoCCNqVamyfLHNrygU3IoBSbv5U~axGHJ3o0FRt2SwXzNMtVSjHcxEwEwLAiKB~sIiF2HSzSmGZoryhDghxS87RhiUbXj0QVfr1lur6WYt~QEZEYqWvUTyeT210ihihUj46ebFoP5waGNzbwqH3QkA3n1S2v7Kftd1e0YNnZOPoQDJZByVlEGKLfhMrMpz9ZolBdqMtVsFtqWdJTHWMT5cwzwS2KdFv3U4F4Ce3RPj193x2xsAE73bciUQisLY0Mp2NGBebJLWxHg2Unq00Gp9kpq3uaVDd3riu24LLz-1OuYGSvD4jMm-buAHqykv~bvQoGh1Zub9oCsMh7FqXQ__)

---

## 7. Problema de Compatibilidad (SDK Version)

Al intentar escanear el código QR, es común encontrarse con errores de compatibilidad si las versiones no coinciden. Al revisar la configuración de **Expo Go** en mi dispositivo, noté que solo soportaba el **SDK 54**.

### Configuración de mi Expo Go
![Configuración Expo Go](https://private-us-east-1.manuscdn.com/sessionFile/6VKii6jHNM5Cs1F6PPSGtt/sandbox/2pLM4qBivWGbewJUtXLCmf-images_1780469813996_na1fn_L2hvbWUvdWJ1bnR1L1JlYWN0TmF0aXZlLUV4cG8vaW1nL3N1cHBvcnRTREs.jpg?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvNlZLaWk2akhOTTVDczFGNlBQU0d0dC9zYW5kYm94LzJwTE00cUJpdldHYmV3SlV0WExDbWYtaW1hZ2VzXzE3ODA0Njk4MTM5OTZfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwxSmxZV04wVG1GMGFYWmxMVVY0Y0c4dmFXMW5MM04xY0hCdmNuUlRSRXMuanBnIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzk4NzYxNjAwfX19XX0_&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=WB39FUQAHLk9AZmi1fAAuFUo6UWsbqPaArRalDVyP936Hh9~5pyrNcQb6bvhz-VWlMSG1lYeEmkG3zwyMJ7nAlxAt8bEc-cH6LXVQkZg8FFEtcdpqcru2VBHqJf3KGTjmsP3Evc8a4kfALw-OuA6zHiaE5dqeh1pm~11dLWHxJd8FsrK1V34qtJ3UkdxFxFAuT17Pz9HRuDMLZ46qF4Exp3zz0c5VEU~fPSX6kBUkplSm7evY7k0rweY9coLAl2oTl1rJ0tAxkwXAeaE33ROPOWejV~0xv5d81~2YzjPZfd-YVhrGD5Uj-ae3JM~hsDLhieye1EhF6IfEidZSPC3Ag__)

> **Nota:** La aplicación indicaba:
> * **Client Version:** 54.0.8
> * **Supported SDK:** 54

Investigando en la comunidad, confirmé que otros usuarios reportaban el mismo inconveniente con las versiones más recientes.

### Comentarios de usuarios en Google Play
![Comentarios Google Play](https://private-us-east-1.manuscdn.com/sessionFile/6VKii6jHNM5Cs1F6PPSGtt/sandbox/2pLM4qBivWGbewJUtXLCmf-images_1780469813996_na1fn_L2hvbWUvdWJ1bnR1L1JlYWN0TmF0aXZlLUV4cG8vaW1nL2NvbW1lbnRHb29nbGVQbGF5.jpg?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvNlZLaWk2akhOTTVDczFGNlBQU0d0dC9zYW5kYm94LzJwTE00cUJpdldHYmV3SlV0WExDbWYtaW1hZ2VzXzE3ODA0Njk4MTM5OTZfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwxSmxZV04wVG1GMGFYWmxMVVY0Y0c4dmFXMW5MMk52YlcxbGJuUkhiMjluYkdWUWJHRjUuanBnIiwiQ29uZGl0aW9uIjp7IkRhdGVMZXNzVGhhbiI6eyJBV1M6RXBvY2hUaW1lIjoxNzk4NzYxNjAwfX19XX0_&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=E74CX9nHmlg7L2knjP9fBEGirkLrQMSiiTTeGjSxHQSn1zrIhGbCwGXpt1rtI4G1TQdKrvkDB13fHfmH3bRNR0BHd6qX5o-67hrC1jYawBAbF95FsQ0cxFieF2PasggvfxXNozXqIXURsj-e-D7zPXba1zRJKOpiM96efEjiHAYH-vHED3YJz3CL4Bsr~lmnTISTdf0qxmHO1NTOlS84uhHtsnDgZsd4YKcmFzBlrgBkYa3T0p62gC20x3qtlopUuB17Ac87V2MWAKcZ89Ue2Ati9wBmX9CQjytQ27GpnbZs4mQ0oVV97lHz5yrmeQxONrrBO~XTtfm4TsPY78fUow__)

El problema radicaba en que `npx create-expo-app@latest` generó un proyecto con **SDK 56**, incompatible con mi versión de cliente móvil.

---

## 8. Solución: Downgrade a Expo SDK 54

Para resolver esto, realicé un "downgrade" forzado a la versión compatible utilizando el siguiente comando:

```bash
npx expo install expo@~54.0.0
```

### Proceso de instalación de SDK 54
![Instalación Expo V54](https://private-us-east-1.manuscdn.com/sessionFile/6VKii6jHNM5Cs1F6PPSGtt/sandbox/2pLM4qBivWGbewJUtXLCmf-images_1780469813996_na1fn_L2hvbWUvdWJ1bnR1L1JlYWN0TmF0aXZlLUV4cG8vaW1nL0V4cG9WNTQ.jpg?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvNlZLaWk2akhOTTVDczFGNlBQU0d0dC9zYW5kYm94LzJwTE00cUJpdldHYmV3SlV0WExDbWYtaW1hZ2VzXzE3ODA0Njk4MTM5OTZfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwxSmxZV04wVG1GMGFYWmxMVVY0Y0c4dmFXMW5MMFY0Y0c5V05UUS5qcGciLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=kGd~KqylNjG9zTag0jxUltkUik2swepAk5TfP3OJbToVzTcx4FpsCyYrTglfzu3YfFzw4ACKEKfnn12Wx9G78oCtm7itlcc6WJn1TiOxnJWETNaE00x3RK82JKSfn-b69NMoNDeaw6KD2jgQvsFQkybaiJk0q7mpDFhpP-RE4TsAJpNmRiIjzPOxHTN3HXlcEfp6KSJZP1BJS-JAawtNG2V7f0AiDPajnfwUkulL7R7mN7qCSTHIZye1HMcANPjo0zpRqcsyqMz6SIq7JDiSRkMrbxX-hyc4hCgSohWk-8gEP4CG1Ig7WSU1AInjq3OlZXKBMTVw7NqKn5k~NPfUJQ__)

Posteriormente, ejecuté una corrección automática de dependencias para asegurar la estabilidad del proyecto:

```bash
npx expo install --fix
```

Y verifiqué la versión final:

```bash
npx expo --version
```

---

## 9. Vinculación Exitosa

Tras ajustar la versión del SDK, el escaneo del código QR funcionó correctamente. La aplicación móvil mostró los pasos finales para completar la carga.

### Pasos finales en Expo Go
![Pasos Expo Go](https://private-us-east-1.manuscdn.com/sessionFile/6VKii6jHNM5Cs1F6PPSGtt/sandbox/2pLM4qBivWGbewJUtXLCmf-images_1780469813996_na1fn_L2hvbWUvdWJ1bnR1L1JlYWN0TmF0aXZlLUV4cG8vaW1nL1N0ZXBzRXhwb01vdmls.jpg?Policy=eyJTdGF0ZW1lbnQiOlt7IlJlc291cmNlIjoiaHR0cHM6Ly9wcml2YXRlLXVzLWVhc3QtMS5tYW51c2Nkbi5jb20vc2Vzc2lvbkZpbGUvNlZLaWk2akhOTTVDczFGNlBQU0d0dC9zYW5kYm94LzJwTE00cUJpdldHYmV3SlV0WExDbWYtaW1hZ2VzXzE3ODA0Njk4MTM5OTZfbmExZm5fTDJodmJXVXZkV0oxYm5SMUwxSmxZV04wVG1GMGFYWmxMVVY0Y0c4dmFXMW5MMU4wWlhCelJYaHdiMDF2ZG1scy5qcGciLCJDb25kaXRpb24iOnsiRGF0ZUxlc3NUaGFuIjp7IkFXUzpFcG9jaFRpbWUiOjE3OTg3NjE2MDB9fX1dfQ__&Key-Pair-Id=K2HSFNDJXOU9YS&Signature=KidGqaDthquxwZ6VZLuJUeuprT8EAoaWig0K6TBr61btUwPEgdmb6Lft26v0PgJSupiWgYOJZ9D6iaSyA7sJmxD9WuSvjIE2RHpP06Vq5Hs3wmitwpJsb~erOhScfGrDyhLwfQbZEp5POPs8oMHW~Y6mbISmjjs-4A2fmGSbAOhPzPmF4sSilTJ5JjtXoxGsajNK4NbMY4nTAiH9w2DvzoKEXHCIimyvSE0F938ywlooAdwMX3ganXcaMnz1euYWKPRVfJA-p48~L4a1Yvr1qNQq6YwqQeh-8uPa~muefYK7NXZXdXC2wFYQB0gxEuR0W6q2TLjWkXZtvAxZYct3sA__)

Ahora, el dispositivo móvil está sincronizado y cualquier cambio guardado en el código se refleja instantáneamente (Fast Refresh).

---

## Estructura del Proyecto

```text
ReactNative-Expo/
│
├── img/                       # Capturas de pantalla y recursos visuales
│   ├── chargeExpomovil.jpg
│   ├── commentGooglePlay.jpg
│   ├── ExpoV54.jpg
│   ├── npxExpoStart.jpg
│   ├── StepsExpoMovil.jpg
│   └── supportSDK.jpg
│
├── ReactNativeWithExpo/       # Código fuente del aplicativo
│   ├── app/
│   ├── assets/
│   ├── node_modules/
│   ├── package.json
│   └── app.json
└── Apuntes_Mejorados.md       # Este archivo
```

---

## Conclusión

La creación de un proyecto con Expo es sumamente ágil, pero la **compatibilidad de versiones** es un factor crítico. Siempre es recomendable verificar qué SDK soporta tu aplicación **Expo Go** antes de iniciar un desarrollo extenso para evitar fricciones técnicas.
