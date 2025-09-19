# 🎶 Algoritmia Compiler

**Algoritmia** es un compilador e intérprete diseñado para un lenguaje educativo que combina **programación estructurada** con **notación musical**.  
El proyecto permite escribir programas en el lenguaje Algoritmia, compilar y generar automáticamente **partituras en PDF**, así como **archivos MIDI y WAV** reproducibles.

---

## 📌 Características principales
- Lenguaje propio: **Algoritmia**, definido con **ANTLR4**.  
- Ejecución de programas con estructuras clásicas: variables, listas, asignaciones, condicionales y bucles.  
- Soporte para **notas musicales** (ej. `A4`, `C5`) y listas de notas.  
- Generación de partituras con **LilyPond**.  
- Conversión a **MIDI** y **WAV** usando **TiMidity++**.  
- Interfaz web en **Flask** con editor integrado para compilar y descargar resultados.  

---

## 🛠️ Estructura del proyecto
- `algoritmia.g4` → Gramática del lenguaje Algoritmia (ANTLR4).  
- `algoritmia.py` → Intérprete principal en Python.  
- `converter.py` → Conversión de notas a formato LilyPond y generación de archivos PDF/MIDI/WAV.  
- `app.py` → Servidor Flask con API para compilar programas Algoritmia desde la web.  
- `index.html` → Interfaz web con editor y botones de descarga.  

---

## 🚀 Instalación y uso

### Requisitos
- Python 3.8+  
- [ANTLR4](https://www.antlr.org/)  
- [LilyPond](https://lilypond.org/)  
- [TiMidity++](https://sourceforge.net/projects/timidity/)  
- Flask  

Instala dependencias:
```bash
pip install flask antlr4-python3-runtime
```

### Uso por consola
Compila y ejecuta un archivo `.alg`:
```bash
python algoritmia.py ejemplo.alg
```

### Uso con interfaz web
Ejecuta el servidor Flask:
```bash
python app.py
```
Abre en el navegador: [http://localhost:5000](http://localhost:5000)  
Escribe tu código en Algoritmia, compila y descarga los resultados en PDF, MIDI y WAV.  

---

## 🎼 Ejemplo en Algoritmia
```alg
VAR notas = [C, D, E, F, G]
REPRODUCIR notas
```
Genera una partitura con las notas **Do, Re, Mi, Fa, Sol**.  

---

## 📂 Archivos generados
- `out.pdf` → Partitura en formato PDF.  
- `out.mid` → Archivo MIDI reproducible.  
- `out.wav` → Archivo de audio WAV.  

---

## 👨‍💻 Autor
Desarrollado con ❤️ por **Juefecito**  
