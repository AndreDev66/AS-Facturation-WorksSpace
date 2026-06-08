# Sistema de Facturación AS — v2.7

> Interfaz de escritorio para facturación, gestión de inventario, clientes y reportes, construida con `CustomTkinter` y SQLite.

---

## 🚀 Descripción

Este proyecto es un sistema de facturación integral diseñado para pequeñas y medianas empresas. Permite gestionar ventas, inventario, clientes, facturas y reportes desde una aplicación de escritorio amigable y moderna.

El proyecto utiliza:
- `tkinter` + `customtkinter` para UI
- `SQLite` para almacenamiento local persistente
- `matplotlib` para gráficos y reportes
- `openpyxl` para exportar datos a Excel (si está instalado)
- `Pillow` para carga de imágenes y logos

---

## ✨ Características principales

- Punto de venta con búsqueda rápida de productos
- Registro de clientes con campos ampliados
- Gestión completa de inventario
- Creación, edición y seguimiento de facturas
- Control de pagos y créditos
- Reportes visuales con gráficos
- Backup automático en `billing_data.json`
- Roles de usuario: `admin` y `empleado`
- Interfaz responsiva y actualizable
- Guardado en SQLite y respaldo JSON

---

## 🧩 Estructura del proyecto

- `Main.py` — archivo principal que arranca la aplicación, muestra pantalla de splash y login.
- `db.py` — módulo de base de datos, inicializa tablas SQLite y gestiona el estado.
- `requirements.txt` — dependencias Python.
- `billing_data.json` — respaldo de datos generado por la aplicación.
- `Excel/` — carpeta de exportaciones o reportes Excel.
- `img/` — recursos de imágenes y logos.
- `test_create_user.py`, `test_login_ui.py` — pruebas de UI/usuario.

---

## ⚙️ Requisitos

- Python 3.10+ recomendado
- Windows (probado en este entorno)

Dependencias principales:
- `customtkinter`
- `matplotlib`
- `Pillow`
- `openpyxl` (opcional, para exportar a Excel)

---

## 💻 Instalación

1. Abre una terminal en la carpeta del proyecto.
2. Crea un entorno virtual (recomendado):

```bash
python -m venv .venv
```

3. Activa el entorno virtual:

```powershell
.\.venv\Scripts\Activate.ps1
```

4. Instala dependencias:

```bash
pip install -r requirements.txt
```

> Si `openpyxl` no está en `requirements.txt`, puedes instalarlo por separado:
>
> ```bash
> pip install openpyxl
> ```

---

## ▶️ Ejecución

Ejecuta la aplicación desde la terminal:

```bash
python Main.py
```

El proyecto abre una ventana de login/splash y luego carga el sistema de facturación.

---

## 🔐 Credenciales iniciales

La base de datos inicial crea un usuario administrador por defecto:

- Usuario: `admin`
- Contraseña: `admin`

> Se recomienda cambiar estas credenciales en el primer inicio.

---

## 📝 Notas importantes

- Los datos se almacenan en `billing.db` y se respaldan en `billing_data.json`.
- Si la app detecta una base de datos vacía, intenta restaurar desde el JSON de respaldo.
- La app incluye migraciones de esquema para mantener compatibilidad con versiones anteriores.
- El diseño permite que el rol `empleado` tenga acceso restringido a edición/eliminación de recursos.

---

## 📌 Mejores prácticas

- Haz respaldos periódicos de `billing.db` y `billing_data.json`.
- Usa la carpeta `Excel/` para guardar reportes exportados.
- Si usas iconos o logos personalizados, colócalos en `img/`.

---

## 🌟 Extensiones posibles

- Exportar facturas en PDF
- Integrar impresión directa de tickets
- Conexión a servicios de cotización de moneda en tiempo real
- Añadir control de usuarios y permisos más granular

---

## 📚 Referencias rápidas

- Archivo principal: `Main.py`
- Datos persistentes: `db.py`
- Respaldo JSON: `billing_data.json`
- Dependencias: `requirements.txt`

---

¿Quieres que agregue también un diagrama rápido de flujo o un ejemplo de uso paso a paso?"
