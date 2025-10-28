# 🏀 Rotowire INJURY REPORT EUROLEAGUE

Este repositorio **recopila y archiva automáticamente el injury report **Euroleague** publicadas por [RotoWire](https://www.rotowire.com/euro/injury-report.php).  
Los datos se almacenan en formato CSV mediante un flujo automatizado de **GitHub Actions**.

---

## 📋 Qué hace este repositorio

- Ejecuta un script en R que extrae el Injury Report desde RotoWire.  
- Añade una **marca temporal** para saber cuándo se obtuvieron los datos.  
- Guarda los resultados como un **archivo CSV con fecha** dentro de la carpeta `data/`.  
- Se ejecuta **a diario** y también **bajo demanda** mediante GitHub Actions.  
- Realiza commit y push automáticos de los nuevos archivos, creando un **archivo histórico** de cuotas del Injuery report a lo largo del tiempo.

---

## ⚙️ Cómo funciona

1. El flujo de trabajo de **GitHub Actions** se activa:
   - Automáticamente cada día a las **10:30 PM UTC**.  
   - Manualmente desde el botón **“Run workflow”** en la pestaña *Actions*.
2. Configura un entorno **R** en un runner Linux.  
3. Instala los paquetes necesarios (`jsonlite`, `dplyr`) y dependencias del sistema.  
4. Ejecuta el script `injuryrport_euroleague.R`, que descarga y guarda los datos actualizados.  
5. Hace commit y push de los nuevos CSV al repositorio, manteniendo un registro completo de la evolución de las cuotas.


---

## 🗓️ Ejemplo de archivo generado

euroleage_injuryreport_2025_10_28.csv

Cada archivo contiene los datos del Injury Report de la Euroleague en el momento en que fueron extraídos, junto con la fecha correspondientes.

