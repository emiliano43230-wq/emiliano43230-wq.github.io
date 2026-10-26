cat > custom.css << 'EOF'
body{background-color:#f8f9fa;font-family:-apple-system,BlinkMacSystemFont,"Helvetica Neue",Arial,sans-serif;color:#333;margin:0;padding:20px}
.jolla,.postcard,.postcard-body{max-width:900px;margin:40px auto;background:#fff;border-radius:12px;box-shadow:0 4px 20px rgba(0,0,0,.08);padding:40px;display:flex;align-items:center;gap:40px}
.jolla-image,.postcard-image,.image-container{flex:0 0 180px}
img,.jolla-image img,.postcard-image img{width:180px;height:180px;border-radius:50%;object-fit:cover;border:4px solid #4682b4;box-shadow:0 2px 10px rgba(70,130,180,.3)}
.jolla-content,.jolla-body,.postcard-content,.content{flex:1}
h1{color:#2c3e50;margin-top:0;font-size:2em;border-bottom:2px solid #4682b4;padding-bottom:8px;display:inline-block}
h4{color:#2c3e50;margin-top:24px;margin-bottom:8px}
ul{list-style:none;padding:0;margin:16px 0}
ul li{margin:10px 0;font-size:1.05em}
ul li a{color:#4682b4;text-decoration:none;transition:color .2s ease}
ul li a:hover{color:#2c3e50;text-decoration:underline}
p{line-height:1.6;color:#555}
@media(max-width:640px){.jolla,.postcard,.postcard-body{flex-direction:column;text-align:center;padding:24px;gap:20px}h1{display:block}img,.jolla-image img,.postcard-image img{width:140px;height:140px}}
EOF
cat > index.Rmd << 'EOF'
---
title: "Emiliano Ramírez"
image: "images/IMG_6073.JPG"
links:
  - label: '`r fontawesome::fa(name = "github", fill = "steelblue")` Github'
    url: "https://github.com/emiliano43230-wq"
  - label: '`r fontawesome::fa(name = "envelope", fill = "steelblue")` Mail'
    url: "mailto:emiliano43230@gmail.com"
output:
  postcards::jolla:
    css: custom.css
---

```{r load_packages, message=FALSE, warning=FALSE, include=FALSE}
library(fontawesome)
