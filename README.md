---
title: "Emiliano Ramírez"
image: images/IMG_6073.JPG
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

### 🔑 Los dos cambios que hice

1. **`Images:` → `image:`** — es la clave que `postcards::jolla` reconoce para la foto de perfil.
2. **`IMG_6073.JPG` → `images/IMG_6073.JPG`** — la ruta debe apuntar a donde está la imagen dentro del repo. Si la subiste a la carpeta `images/`, esa es la ruta correcta. Si la subiste a la raíz del repo, déjala como `image: IMG_6073.JPG`.

---

### ⚠️ Detalles que pueden hacer que no se vea

- **Ruta relativa al `.Rmd`**: la ruta en `image:` es relativa al archivo `index.Rmd`. Como está en la raíz del repo y la imagen está en `images/`, `images/IMG_6073.JPG` es correcto.
- **Mayúsculas exactas**: `IMG_6073.JPG` ≠ `img_6073.jpg`. En GitHub Pages (Linux) importan. Verifica con `ls images/`.
- **Espacios o acentos en el nombre**: si el archivo tuviera espacios, tendrías que escribir `image: "images/mi imagen.jpg"` entre comillas. Aquí no aplica.
- **Recuerda re-renderizar y subir**: después de editar el `.Rmd`, corre:

  ```bash
  quarto render index.Rmd
  git add .
  git commit -m "Corrige YAML: usa image: con ruta correcta"
  git push origin main
