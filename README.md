---
title: "Emiliano Ramírez"
image: "images/IMG_6073.JPG"
links:
  - label: '`r fontawesome::fa(name = "github", fill = "steelblue")` Github'
    url: "https://github.com/emiliano43230-wq"
  - label: '`r fontawesome::fa(name = "envelope", fill = "steelblue")` Mail'
    url: "mailto:emiliano43230@gmail.com"
output:
  postcards::jolla
---

```{r load_packages, message=FALSE, warning=FALSE, include=FALSE} 
library(fontawesome)


---

### 🔑 Los cambios clave que hice

1. **`Images:` → `image:`** : La plantilla `jolla` solo reconoce la clave `image` (en singular y minúscula) para mostrar la foto de perfil[reference:1].
2. **Ruta de la imagen** : Usé `images/IMG_6073.JPG` para que apunte a la carpeta donde la guardaste. Si la imagen está en la raíz del repositorio, cámbialo a `"IMG_6073.JPG"`.
3. **Formato de enlaces** : Mantuve la estructura de lista con iconos de Font Awesome, igual que en el ejemplo[reference:2].

---

### 🚀 Pasos finales para que se vea en tu sitio

1. **Renderiza el archivo** (esto es indispensable, ya que GitHub Pages sirve el HTML generado, no el `.Rmd`):
   ```bash
   quarto render index.Rmd
