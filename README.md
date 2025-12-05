# Práctica entregable Unidad 01: CI/CD y Documentación

Esta es la entre para la práctica de documentación automatica.
## Ver la documentación
[Ver repositorio aquí](https://github.com/agarram12/Despliegue-Aplicaciones)

---------
## Pasos que se piden y cómo se ha realizado.
### 1. Herramientas utilizadas:
De las que se ofrecían en la práctica he elegido pdoc para Python. Lo he elegido porque es una opción sencilla, ya que solo hay que poner el código e indicar donde está nuestro archivo al que le queremos generar el HTML automático

El comando para generarlo que he usado (en mi caso y en el del repositorio) ha sido:
`pdoc -o docs principal.py`

### 2. Workflows con GitHub Action
He creado la ruta de carpetas de `.github/workflows` con un archivo .YML que hace lo siguiente:
1. Detecta cuando se hace un push en la rama main
2. Se instala python y pdoc para poder realizar la documentación
3. Ejecuta un comando que crea la carpeta `docs` como en el ejemplo original
4. Se sube esa carpeta a una rama llamada `gh-pages` para que pueda verse en internet

---------

## Cuestionario de evaluación

| Pregunta | Respuesta |
| :--- | :--- |
| **a) Herramienta** | He usado **pdoc**. Ya que es una utilidad moderna y genera el archivo HTML sin tener que configurar nada a diferencia de otras como Sphinx. |
| **b) Código documentado** | En mi archivo `principal.py` he usado las comillas triples para hacer un bloque de "texto" donde documentar el código. |
| **c) Configuración Pages** | He usado la acción  de gh-pages en mi repositorio y en la configuración del repo (Settings > Pages) he elegido la rama `gh-pages` para que de ahí ejecute pages. |
| **d) Colaboración** | Me parece muy util ya que al trabajar con alguien no tienen que instalar ni generar el HTML por su cuenta, siempre pueden irse mediante el enlace a la web y ver la última versión de toda la documentación cada vez que se actualice. |
| **e) Mensajes de commit** | Cada vez que he hecho un commit he intentado ser descriptivo, por ej: "Correción del archivo pdoc en YML" o "Añado HTML y archivos de automatización" para saber que he hecho en cada paso. |
| **f) Accesibilidad vs Privacidad** | GitHub Pages permite que la documentación sea pública aunque mi código fuente esté en un repositorio completamente privado. |
| **g) Dónde está explicado** | Las instrucciones de uso y el enlace a la web están justo al principio de este README, para que sea lo primero que se vea al abrirlo. |
| **h) CI/CD** | Esto es CI/CD porque se hacen pruebas y se construye al subir los cambios y es despliegue continuo debido a que la web se actualiza y se publica ella sola sin necesidad de que yo toque nada. El evento que haces que suceda es el `push`. |
| **i) Multiformato (Extra)** | También he generado la documentacion con Markdown usando la misma herramienta pdoc. Guardando el resultado de esto en una carpeta distinta y usando una acción para que se pueda descargar desde la pestaña de actions del repositorio |

### Conclusión
Me parece una herramienta muy útil e intuitiva ya que apenas requiere conocimientos, al principo tuve algunos problemas con el comando principalemente por la instalación y por unos errores en los nombres, por lo demás me ha sido muy sencillo de usar y bastante interesante.