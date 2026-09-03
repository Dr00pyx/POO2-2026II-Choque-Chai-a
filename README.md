# Laboratorio POO2: Refactorización SOLID - Gestor Académico

**Estudiante:** Choque Chaiña  
**Curso:** Programación Orientada a Objetos 2 (POO2)  
**Periodo Académico:** 2026-II  
**Repositorio:** `Dr00pyx/POO2-2026II-Choque-Chai-a`  

---

## 📌 Descripción del Proyecto

Este proyecto aborda la refactorización de un sistema monolítico de gestión de notas e historial académico (*Gestor Académico*). La solución original presentaba problemas severos de acoplamiento, duplicación de código y violaciones a los principios SOLID. 

Se implementó una arquitectura limpia desacoplada aplicando los principios **SRP** (Responsabilidad Única) y **DIP** (Inversión de Dependencias) tanto en **Python 3.12+** como en **C++20**.

---

## 🚀 Requisitos del Sistema

* **Python:** Versión 3.12 o superior.
* **C++ Compiler:** `g++` con soporte para C++20 (o C++17).
* **Framework de Pruebas:** `pytest` para entorno Python.

---

## 🛠️ Ejecución y Pruebas

### 1. Módulo Python (`parte2_gestor_academico`)

Para ejecutar la suite de pruebas automatizadas en memoria:

Módulo C++20 (parte2_gestor_academico)
PowerShell
# Compilar y ejecutar la versión refactorizada
cd parte2_gestor_academico
g++ -std=c++20 main.cpp -o main.exe
.\main.exe

🏛️ Decisiones de Arquitectura
Inversión de Dependencias (DIP): Se definió una interfaz abstracta para los servicios de auditoría (AuditoriaInterface / IAuditoriaService). Esto permite inyectar implementaciones concretas como AuditoriaArchivo para producción o AuditoriaNull para la ejecución de pruebas sin acceso a disco.

Encapsulamiento de Dominio: La entidad Estudiante valida de forma estricta las notas en el rango [0.0, 20.0] mediante lanzamiento de excepciones (ValueError), protegiendo la integridad del sistema.

Separación de Responsabilidades (SRP): El cálculo de promedios, la gestión del repositorio en memoria y la generación de reportes CSV se dividieron en clases independientes.

Estructura del Repositorio
POO2-2026II-Choque-Chai-a/
├── docs/
│   └── Informe_Parte2_Refactor.pdf    # Informe Técnico de 8 Puntos
├── parte1_gestor_academico/           # Código base e implementación inicial
└── parte2_gestor_academico/           # Versión Refactorizada + Pruebas
    ├── gestor_academico_base.py       # Monolito original Python
    ├── gestor_academico_base.cpp      # Monolito original C++
    ├── gestor_academico.py            # Dominio e interfaces refactorizadas
    ├── main.cpp                       # Código refactorizado en C++20
    └── test_gestor_academico.py       # Suite de pruebas unitarias (pytest)

```powershell
cd parte2_gestor_academico
pytest test_gestor_academico.py -v
