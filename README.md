# Sistema de Votaciones (Flask + MySQL)

Aplicación web para:
- Registrar ciudadanos con su puesto de votación.
- Consultar el puesto de votación por número de identificación.

## Requisitos
- Python 3.10+
- MySQL Server

## Instalación
1. Crear y activar entorno virtual:
   ```powershell
   py -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```
2. Instalar dependencias:
   ```powershell
   pip install -r requirements.txt
   ```
3. Crear la base de datos y tablas:
   - Ejecuta el script `database/schema.sql` en tu servidor MySQL.

## Configuración de conexión
La app usa variables de entorno opcionales:
- `DB_HOST` (default: `localhost`)
- `DB_PORT` (default: `3306`)
- `DB_USER` (default: `root`)
- `DB_PASSWORD` (default: vacío)
- `DB_NAME` (default: `votaciones_db`)

Ejemplo en PowerShell:
```powershell
$env:DB_HOST = "localhost"
$env:DB_USER = "root"
$env:DB_PASSWORD = ""
$env:DB_NAME = "votaciones_db"
```

## Ejecución
```powershell
python app.py
```

Luego abre:
- [http://127.0.0.1:5000](http://127.0.0.1:5000)
