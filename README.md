# Trabajo práctico: búsqueda de ligandos

## Abrir la notebook en Google Colab

1. Abrí la notebook con este enlace:

   [Abrir la notebook en Colab](https://colab.research.google.com/github/mcpalumbo/tp-ligandos/blob/main/TP_blancos_compuestos_Colab.ipynb)

3. En Colab elegí **Entorno de ejecución → Ejecutar todas** o ejecutá las celdas en orden.

La primera parte prepara el entorno y descarga los datos desde este repositorio. No es necesario instalar Python en la computadora ni descargar los archivos manualmente.

## ¿Qué vamos a hacer?

- Priorizar blancos moleculares de *Mycoplasma pneumoniae* con evidencias de drogabilidad, esencialidad, off-targets y centralidad.
- Explorar filtros interactivos y construir un ranking modificable.
- Analizar LigA (UniProt P78021) y visualizar su Pocket 1.
- Consultar LigQ2 Web con secuencias FASTA y examinar proteínas homólogas, ligandos conocidos y candidatos similares.
- Comparar la posición cristalográfica del inhibidor 1X7 con el pocket predicho de P78021 mediante alineamiento estructural.
- Calcular propiedades fisicoquímicas y predicciones ADMET para los compuestos recuperados.
- Explorar Boltz-2 de forma opcional si hay tiempo y Colab asigna GPU.

## Archivos del repositorio

La carpeta [`datos_tp/`](datos_tp/) contiene todos los archivos pequeños que usa la notebook: tabla de FastTarget, secuencias FASTA, modelos estructurales, archivos de pockets y una salida de LigQ2 de respaldo.

La salida de respaldo permite continuar aunque LigQ2 Web esté temporalmente ocupada. Para consultar LigQ2 Web, la notebook también genera archivos FASTA descargables desde Colab, porque el selector de archivos del navegador no puede acceder directamente al sistema de archivos interno de Colab.

## Recomendaciones de trabajo

- Ejecutá las celdas en orden; algunas variables se crean en celdas anteriores.
- En la Parte I mové los selectores de los filtros y observá cómo cambia el número de candidatos. Luego ejecutá los gráficos y el ranking.
- En LigQ2 distinguí siempre entre proteína relacionada, ligando conocido y compuesto predicho por similitud.
- Un score alto, un Tanimoto alto o una predicción ADMET favorable no demuestran actividad experimental.
- Guardá una copia propia de la notebook si querés conservar tus exploraciones.

## Target Pathogen
[Abrir Target Pathogen Web](http://targetsbg.cluster.qb.fcen.uba.ar/patho/)

## LigQ2 Web

[Abrir LigQ2 Web](https://ligq.infra.cluster.qb.fcen.uba.ar)

La notebook indica cuándo descargar los FASTA y cómo cargar el ZIP de resultados. Si el servicio no responde, podés trabajar con la salida de respaldo incluida.

## Otros repos

[FastTarget](https://github.com/mcpalumbo/fasttarget)

[LigQ2](https://github.com/gschottlender/LigQ_2)
