# Laboratorio POO2: Refactorización SOLID - Gestor Académico

**Estudiante:** Choque Chaiña  
**Curso:** Programación Orientada a Objetos 2 (POO2)  
**Periodo Academicó:** 2026-II  
**Repositorio:** `Dr00pyx/POO2-2026II-Choque-Chai-a`  

---

## 📌 Descripción del Proyecto

Este proyecto aborda la refactorización de un sistema monolítico de gestión de notas e historial académico (*Gestor Académico*). La solución original presentaba problemas severos de acoplamiento, duplicación de código y violaciones a los principios SOLID. 

Se implementó una arquitectura limpia desacoplada aplicando los principios **SRP** (Responsabilidad Única) y **DIP** (Inversión de Dependencias) tanto en **Python 3.12+** como en **C++20**.

---

## 🚀 Requisitos del Sistema

* **Python:** Version 3.12 o superior.
* **C++ Compiler:** `g++` con soporte para C++20 (o C++17).
* **Framework de Pruebas:** `pytest` para entorno Python.

---

## 🛠️ Ejecución y Pruebas

### 1. Módulo Python (`parte2_gestor_academico`)

Para ejecutar la suite de pruebas automatizadas en memoria:

```powershell
cd parte2_gestor_academico
pytest test_gestor_academico.py -v
