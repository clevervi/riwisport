# Análisis de Datos - RIWI Sport

## Descripción
Análisis de comportamiento de clientes y ventas para RIWI Sport, comercio de artículos deportivos en Colombia. Este proyecto cumple con los requisitos de la Prueba de Desempeño en Analítica de Datos.

## Requisitos Previos
- PostgreSQL instalado y ejecutándose
- Python 3.8 o superior
- Archivo `RiwiSport.sql` restaurado en PostgreSQL

## Instalación y Configuración

### 1. Restaurar la Base de Datos
```bash
psql -U tu_usuario -d RiwiSport -f RiwiSport.sql
```

### 2. Instalar Dependencias de Python
```bash
pip install -r requirements.txt
```

### 3. Configurar Variables de Entorno
- Copiar el archivo `.env.example` a `.env`
- Editar el archivo `.env` con tus credenciales:

```env
DB_HOST=localhost
DB_PORT=5432
DB_NAME=RiwiSport
DB_USER=tu_usuario_postgres
DB_PASSWORD=tu_contraseña_postgres
```

### 4. Ejecutar el Análisis
```bash
jupyter notebook analisis_RIWI_Sport.ipynb
```

## Estructura del Proyecto

```
proyecto_riwisport/
├── analisis_RIWI_Sport.ipynb      # Notebook principal con análisis completo
├── analysis_RIWI_Sport.ipynb      # Notebook principal con análisis completo (ingles)
├── requirements.txt               # Dependencias de Python
├── .env                           # Configuración de base de datos (no compartir)
├── README.md                      # Este archivo (español)
├── README_En.md                   # Este archivo (ingles)
├── informe_RIWI_Sport.md          # Resumen ejecutivo del análisis
└── En_informe_RIWI_Sport.md       # Resumen ejecutivo del análisis (ingles)

```

## Dependencias Principales

- **pandas, numpy** - Análisis y manipulación de datos
- **sqlalchemy, psycopg2-binary** - Conexión a PostgreSQL
- **matplotlib, seaborn** - Visualizaciones y gráficos
- **python-dotenv** - Manejo de variables de entorno

## Funcionalidades Implementadas

### ✅ Conexión a Base de Datos
- Conexión segura a PostgreSQL usando SQLAlchemy
- Verificación de conexión exitosa

### ✅ Consultas SQL
- Consultas a tablas: customer, order, order_item, product, category
- Integración de datos en tabla de ventas unificada

### ✅ Análisis con Pandas/NumPy
- **Tendencia central:** Media, mediana, moda del gasto
- **Dispersión:** Varianza, desviación estándar
- **KPIs de negocio:** Ticket promedio, top categorías, top productos

### ✅ Visualizaciones
- Histograma del gasto por cliente
- Boxplot de ventas por categoría
- Gráficos de barras para top categorías y productos

### ✅ Insight Accionable
- Análisis de oportunidades comerciales
- Recomendaciones específicas para RIWI Sport

## Solución de Problemas

### Error de Conexión a la Base de Datos
- Verificar que PostgreSQL esté ejecutándose
- Confirmar credenciales en el archivo `.env`
- Asegurar que la base de datos `RiwiSport` exista

### Dependencias No Encontradas
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### Problemas con Jupyter
```bash
pip install jupyter
jupyter notebook
```
