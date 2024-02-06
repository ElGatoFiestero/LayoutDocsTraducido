# Tipos de Archivos

Esta página contiene una lista de todos los tipos de archivos relacionados con diseños personalizados y temas.

## Archivos SZS

Los archivos `SZS` son archivos comprimidos con un algoritmo de compresión personalizado.
En realidad, son archivos `SARC` (también conocidos como `ARC`). El algoritmo de compresión que se utiliza es Yaz0.

### Estructura

La estructura de un archivo `SZS` de menú suele ser la misma:

```
📦ResidentMenu_11.0.1_original
┣ 📂anim
┃ ┗ 📜[filename].bflan
┣ 📂bgsh
┃ ┣ 📜__ArchiveShader.bnsh
┃ ┗ 📜__ArchiveShader.bushvt
┣ 📂blyt
┃ ┗ 📜[filename].bflyt
┗ 📂timg
  ┗ 📜__Combined.bntx
```


Las carpetas contienen lo siguiente:

- `anim`: Archivos de animación (`.bflan`)
- `bgsh`: Shaders de GPU (`.bnsh`, `.bushvt`)
- `blyt`: Archivos de diseño (`.bflyt`)
- `timg`: Imágenes del menú (`.bntx`)

Para diseños personalizados, solo tocamos los archivos en `anim` y `blyt`. Sin embargo, es interesante tener en cuenta que el instalador NXTheme internamente inyecta la imagen de fondo [nxtheme](../definitions.md#nxtheme) en el archivo `__Combined.bntx`.

### Tipos de Archivos

Nintendo ha estado utilizando sus propios formatos para diseñar menús, animaciones y sombreadores, a menudo almacenados en estos archivos de archivos (s)arc.
Aquí hay una tabla de algunos formatos que han surgido a lo largo de los años:

| Consola                                           | Formato    | Descripción                                          | Documentos y Recursos Adicionales                                                                                                                                                                                                                 |
|---------------------------------------------------|-----------|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wii (Rev/**R**evolution)                          | `(b)rlyt` | (**B**inary) **R**evolution **L**a**Y**ou**T**       |                                                                                                                                                                                                                                          |
|                                                   | `(b)rlan` | (**B**inary) **R**evolution **L**ayout **AN**imation |                                                                                                                                                                                                                                          |
| DS (NTR/Nitro)                                    | -         | -                                                    |                                                                                                                                                                                                                                          |
| 3DS (**C**TR)                                     | `(b)clyt` | (**B**inary) **C**TR **L**a**Y**ou**T**              |                                                                                                                                                                                                                                          |
|                                                   | `(b)clan` | (**B**inary) **C**TR **L**ayout **AN**imation        |                                                                                                                                                                                                                                          |
| Wii U (**C**afe), pero también utilizado por 3DS y Switch | `(b)flyt` | (**B**inary) ca**F**e **L**a**Y**ou**T**             | [Switch Toolbox](https://github.com/KillzXGaming/Switch-Toolbox/blob/c9e74e0be114885f347789f3bd348baccacf0842/File_Format_Library/FileFormats/Layout/CAFE/BFLYT.cs), [3DSkit](https://github.com/Tyulis/3DSkit/blob/master/doc/BFLYT.md) |
|                                                   | `(b)flan` | (**B**inary) ca**F**e **L**ayout **AN**imation       | [Switch Toolbox](https://github.com/KillzXGaming/Switch-Toolbox/blob/c9e74e0be114885f347789f3bd348baccacf0842/File_Format_Library/FileFormats/Layout/CAFE/BFLAN.cs), [3DSkit](https://github.com/Tyulis/3DSkit/blob/master/doc/BFLAN.md) |
| Switch (NX)                                       | `(b)ntx`  | (**B**inary) **N**x **T**e**X**ture                  | [Switch Toolbox](https://github.com/KillzXGaming/Switch-Toolbox/blob/c9e74e0be114885f347789f3bd348baccacf0842/File_Format_Library/FileFormats/Texture/BNTX.cs), [3DSkit](https://github.com/Tyulis/3DSkit/blob/master/doc/BNTX.md)       |


(If you're interested in more Nintendo device codenames, check
out [this page](https://salty-salty-studios.com/shiz/misc/codenames.html))

All these formats are based on the same underlying format, but simply use different names for different consoles.
The underlying format simply goes through several versions. For example, `BFLAN` appears as version such as 7.1.0/7.2.1
on 3DS and
8.6.0 on Switch.

There are a lot more file formats used in all these systems. For a comprehensive list, check
out [this folder on github](https://github.com/KillzXGaming/Switch-Toolbox/tree/master/File_Format_Library/FileFormats),
which can at least give you an idea of all the different formats. Actual documentation will have to be searched for
elsewhere.

Check out these wikis for more information on all kinds of Nintendo file formats:
- [Deep Sea Knowledge/OatMealDome Wiki](https://wiki.oatmealdome.me/Category:File_formats)
- [3DBrew](https://www.3dbrew.org/wiki/Category:File_formats)
- [Custom Mario Kart Wiiki](https://wiki.tockdom.com/wiki/List_of_File_Formats)
- [Switchbrew](https://switchbrew.org/)


### **[Continue to Layouts (bflyt)](layouts/index.md) :octicons-arrow-right-16:**

### **[Continue to Animations (bflan)](animations/index.md) :octicons-arrow-right-16:**
