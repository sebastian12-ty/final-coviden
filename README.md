# COVIDEN Dental v5.0 PREMIUM

## Instalacion
```bash
python -m pip install -r requirements.txt
```

## Configurar APIs
La app arranca sin claves, pero las funciones de IA responderan con un mensaje de configuracion pendiente.

PowerShell:
```powershell
$env:GEMINI_API_KEY="tu_clave_gemini"
$env:GROQ_API_KEY="tu_clave_groq"
```

Opcional:
```powershell
$env:GEMINI_MODEL="gemini-1.5-flash"
$env:GROQ_MODEL="llama-3.3-70b-versatile"
```

## Ejecutar
```bash
python app.py
```

## URLs
| URL | Descripcion |
|-----|-------------|
| http://localhost:5000 | Sitio publico |
| http://localhost:5000/mi-cuenta | Panel del paciente |
| http://localhost:5000/admin | Admin (admin/coviden2024) |
| http://localhost:5000/admin/ver-bd | Visualizar BD |
| http://localhost:5000/admin/backup-db | Descargar backup |

## Notas
- La base SQLite se crea automaticamente en `coviden.db`.
- En carpetas sincronizadas como OneDrive, la app usa `journal_mode=MEMORY` para evitar errores de I/O de SQLite.
- `Pillow>=12.0.0` evita fallos de instalacion en Python 3.14 en Windows.

