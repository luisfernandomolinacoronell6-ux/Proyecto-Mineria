# Proyecto de Minería de Datos: Predicción de Diabetes

**Materia:** Minería de Datos  
**Integrantes:** 
* Dubay Aguirre
* Luis Fernando Molina

## Evaluación del uso de Inteligencia Artificial (Actividad 1 - Tercer corte)

* **Herramienta utilizada:** Gemini AI.
* **Propósito:** Adaptar un notebook de Jupyter al entorno web interactivo de Streamlit, solucionar incompatibilidades gráficas y de visualización, e implementar validación cruzada estratificada para cumplir rigurosamente con la rúbrica del modelado.
* **Prompt principal:** *"Gemini necesito desplegar un codigo de un proyecto que hice con un compañero en streamlit pero no sé cómo usarlo"*, complementado con los ajustes solicitados por la revisión de resultados del profesor sobre el reporte de media y variación.
* **Cómo verificamos la respuesta:** Se validó ejecutando y probando la aplicación web en vivo alojada en Streamlit Community Cloud, comprobando que cargara correctamente las pestañas, los datos limpios y las métricas cruzadas sin arrojar errores en los registros del servidor.
* **Problemas encontrados:** El código original contenía comandos exclusivos de celdas de Jupyter (`display()`, `plt.show()`) que ocasionaban que la página web se quedara en blanco. Además, el esquema inicial del modelo utilizaba únicamente una partición tradicional (`train_test_split`), mientras que la rúbrica exigía obligatoriamente el uso de validación cruzada (`StratifiedKFold`).
* **Ajustes realizados:** 
  1. Se adaptó la interfaz mediante pestañas (`st.tabs`) y comandos nativos para dataframes y gráficos (`st.dataframe`, `st.pyplot`).
  2. Se integró `StratifiedKFold` y `cross_validate` para calcular la media y desviación estándar de las métricas en 5 particiones.
  3. Se añadieron formalmente los nombres de los integrantes y la materia tanto en la aplicación visual como en el repositorio.
