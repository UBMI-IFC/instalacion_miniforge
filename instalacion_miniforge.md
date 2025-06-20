---
theme: seriph
background: # https://cover.sli.dev
title: Operaciones básicas con conda usando miniforge
author: acph
info: |
  ## Guia para conda
  Insatrucciones simples par ausar conda
exportFilename: operaciones_conda
export:
  format: pdf
  dark: false
fonts:
  sans: Roboto
  serif: Roboto Slab
  mono: Fira Code  
class: text-center
transition: slide-left
mdc: true
hideInToc: true
---

<div grid="~ cols-2 gap-60%" m="t--3" > 
<!-- Logo IFC -->
<img border="rounded" src="./ifc.png" alt="">
<!-- Logo UBMI -->
<img border="rounded" src="./ubmi.png" alt="">
</div>

<br>




# Instalación de `miniforge`

## Unidad de Bioinformática y Manejo de la Información, IFC UNAM.

<br>

<a href="https://github.com/UBMI-IFC" target="_blank">
   <carbon:logo-github/>
</a>
<a href="mailto:ubmi@ifc.unam.mx" target="_blank">  <!-- class="slidev-icon-btn"> -->
   <carbon:email/>
</a>
<a href="https://sites.google.com/ifc.unam.mx/ubmi-ifc" target="_blank">  <!-- class="slidev-icon-btn"> -->
   <carbon:network-enterprise/>
</a>
<a href="https://www.youtube.com/@unidaddebioinformaticaifc5165" target="_blank">  <!-- class="slidev-icon-btn"> -->
   <carbon:logo-youtube/>
</a>

[Tutoriales UBMI-IFC](https://ubmi-ifc.github.io/Tutoriales-IFC)


<!-- --- -->
<!-- transition: slide-left -->
<!-- --- -->



---
hideInToc: true
transition: slide-left
layout: two-cols
layoutClass: gap-15
---

# Navegación


|           Atajos de teclado                         |                             |
| --------------------------------------------------- | --------------------------- |
| <kbd>right</kbd> / <kbd>space</kbd>                 | Siguiente paso     |
| <kbd>left</kbd>  / <kbd>shift</kbd><kbd>space</kbd> | Paso anterior |
| <kbd>up</kbd>                                       | Siguiente diapositiva              |
| <kbd>down</kbd>                                     | Diapositiva anterior         |
| <kbd>f</kbd>                                        | _fullscreen_ |

<!-- https://sli.dev/guide/animations.html#click-animation -->

Pasa el _mouse_ por la esquina inferior izquierda para ver la barra de navegación.

<div class="demo-container">
  <svg class="absolute -bottom-28 -left-1 w-80 opacity-50">
    <polygon points="0,0 0,40 260,40 260,0" fill='#abcbca' stroke='#123123'
    stroke-width='2' fill-opacity="0.4" />
  </svg>
</div>

<p v-after class="absolute bottom--2 left-24 opacity-50 transform">Here!</p>

<!-- <img -->
<!--   v-after -->
<!--   class="absolute -bottom-9 -left-7 w-80 opacity-50" -->
<!--   src="https://sli.dev/assets/arrow-bottom-left.svg" -->
<!--   alt="" -->
<!-- /> -->
<!-- <p v-after class="absolute bottom-23 left-45 opacity-30 transform -rotate-10">Here!</p> -->

::right::

# Tabla de contenido

Uso básico de `conda` con `miniforge` usando los canales
`conda-forge` y `bioconda`.

<Toc minDepth="1" maxDepth="1" />


---
layout: statement
---

# ¿Qué es `miniforge`?

`miniforge` es el instalador base para el canal `conda-forge`.

Básicamente se trata de una instalación mínima del lenguaje de programación __Python__ y los gestores de paquetes y ambientes `conda` y `mamba`
configurados con `conda-forge` cómo repositorio de _software_.

También puedes instalar programas __bioinformáticos__ usando el repositorio [`bioconda`](https://bioconda.github.io/).


<br>

Para más información, visita la página web de [conda-forge](https://conda-forge.org/) o el repositorio de [GitHub de miniforge](https://github.com/conda-forge/miniforge).


---
layout: statement
---

# ¿Qué es `conda-forge`

`conda-forge` es un repositorio de paquetes para un gran abanico de "software".

Se trata de un esfuerzo de la comunidad de tener una colección de programas y librerías actualizadas y listas para instalar. 


---
layout: default
---


# Instalación de `miniforge` en **Windows***


<br>

1. Descarga el archivo `.exe` de instalación:

<br>

<div grid="~ cols-2 gap-4">

<div style="grid-placement: center; align-items: center;">
 <a href="https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-Windows-x86_64.exe">
<button type="submit" id="my-button">
  Click en este botón!
</button>
</a>
</div>


<div>
o descárgalo entrando a la página de descarga de 
<a href="https://conda-forge.org/download/" target="__blank">
<b>miniforge</b>
</a>
</div>
</div>

<br>

2. Da doble *click* sobre el archivo descargado y sigue las indicaciones. 
###### Es recomendable hacer la instalación sólo para el usuario y no para todo el sistema.

<br>

3. ¡Listo! Puedes acceder al *prompt* de miniforge dando *click* en el boton de windows (<img style="display: inline-block;" src="./windows.png" alt="Windoqws logo" width="15">).


<!-- </style> -->

<!-- <img src="./windows.png" alt="Windows Image" width="300" height="200"> -->



<footer class="absolute bottom-5 left-5% right-0 p-2"> 
* No está disponible la instalación para procesadores ARM (marzo 2025).
</footer>

<style>
  #my-button {
    background-color: #333;
    color: #fff;
    border-radius: 5px;
    padding: 10px 20px;
  }
  
  #my-button i {
    color: red;
    font-size: 16px;
    margin-left: 10px;
  }
</style>


---
layout: default
---


# Instalación de `miniforge` en **GNU/linux** o **MacOS**


<br>

1. Descarga el _script_ (`.sh`) de instalación correspondiente a tu sistema operativo
de la página de <a href="https://conda-forge.org/download/" target="__blank">*miniforge*</a> o ejecuta el siguiente comando:

```bash
$ wget "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
```

2. Ejecuta el *script* desde una terminal.

```bash
$ bash Miniforge3-$(uname)-$(uname -m).sh
```

3. Sigue las instrucciones que incluyen aceptar la licencia de uso.
###### Es recomendable permitir que se agregue conda a tu `PATH`.

4. Reinicia tu terminal y ¡listo! ya puedes trabajar en el ambiente `base`.

```bash
(base)$_

```

5. Puedes usar `conda` para configurar tu `shell` preferido. Por ejemplo:

```bash
(base)$ conda init fish

```

<!-- </style> -->

<!-- <img src="./windows.png" alt="Windows Image" width="300" height="200"> -->


---
layout: end
---

# ¿Tienes más dudas?

Contáctanos:

[ubmi@ifc.unam.mx](mailto:ubmi@ifc.unam.mx)

## También puedes ver:
- Nuestra presentación de uso de conda -> [AQUI](https://acpooth.github.io/guia_conda/1)
- Nuestro tutorial escrito -> [AQUI](https://ubmi-ifc.github.io/Tutoriales-IFC/manuales/usuarios_ubmi/conda_ambientes_virtuales)


<div style="text-align: center;">
 <PoweredBySlidev mt-10 /> 
</div>




<footer class="absolute bottom-5 left-93% right-0 p-2"> <Link to="2"><div class="i-carbon:home" /></Link>  </footer>

