# Análisis y Procesamiento de Candidatos

Este proyecto realiza la limpieza, procesamiento y análisis de datos de candidatos a empleos, almacenando los resultados en una base de datos MySQL y generando visualizaciones.

## Características
- Carga y limpieza de datos desde `candidates.csv`
- Conversión de tipos de datos
- Filtrado de candidatos con altos puntajes en pruebas técnicas
- Almacenamiento de datos en MySQL
- Generación de gráficos con Matplotlib y Seaborn

## Requisitos
- Python
- MySQL
- Libreria:
  - `pandas`
  - `mysql-connector-python`
  - `matplotlib`
  - `seaborn`

## Instalación
1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/tu-repositorio.git
   cd tu-repositorio
   ```
2. Instala las dependencias:
   ```bash
   pip install pandas mysql-connector-python matplotlib seaborn
   ```
3. Configura la base de datos en MySQL:
   ```sql
   CREATE DATABASE candidates_db;
   USE candidates_db;
   CREATE TABLE candidates (
       id INT AUTO_INCREMENT PRIMARY KEY,
       first_name VARCHAR(50),
       last_name VARCHAR(50),
       email VARCHAR(100),
       country VARCHAR(50),
       application_date DATE,
       yoe INT,
       seniority VARCHAR(50),
       technology VARCHAR(50),
       code_challenge_score FLOAT,
       technical_interview_score FLOAT
   );
   ```
4. Ejecuta el script:
   ```bash
   python script.py
   ```

## Uso
1. El script carga los datos desde `candidates.csv`.
2. Se eliminan valores nulos y se convierten los tipos de datos.
3. Se filtran candidatos con puntajes altos y se guardan en `candidates_cleaned.csv`.
4. Los datos se insertan en MySQL.
5. Se generan visualizaciones sobre contrataciones por tecnología, año, seniority y país.

## Visualizaciones
El script genera gráficos que muestran:
- Distribución de contrataciones por tecnología
- Evolución de contrataciones por año
- Distribución por nivel de seniority
- Comparación de contrataciones por país a lo largo de los años

## Autor
[Simón García](https://github.com/simondev06)
