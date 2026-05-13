# 🚀 Aplicativo Interactivo de Lógica y Registro de Calificaciones

Este repositorio contiene la implementación en pseudocódigo de un **Sistema Interactivo de Lógica, Procesamiento Aritmético y Gestión de Calificaciones** desarrollado en **PSeInt**. El sistema simula un entorno operativo real, garantizando la robustez mediante la validación cíclica de datos y control de flujo dinámico.

---

## 📋 Características del Sistema

El aplicativo está diseñado bajo un enfoque modular y continuo, estructurado en las siguientes secciones principales:

1. **Configuración Inicial del Perfil:** Captura obligatoria y validación del nombre del estudiante y el entorno de desarrollo activo.
2. **Módulo de Operaciones Básicas:** Cálculo numérico de suma, resta, multiplicación y división, incluyendo un mecanismo condicional de mitigación para evitar la división por cero.
3. **Módulo de Registro de Notas:** Inicialización exacta y procesamiento descriptivo de un vector (arreglo unidimensional) de 5 calificaciones, calculando el promedio general, valores extremos (máximo y mínimo) y la clasificación académica.
4. **Persistencia Dinámica Histórica:** Simulación del almacenamiento acumulativo de los reportes generados en memoria dentro de un archivo de texto plano (`resultados.txt`), controlando cambios pendientes mediante banderas lógicas (*flags*).

---

## 🛠️ Requisitos del Entorno

Para ejecutar este proyecto de manera óptima, asegúrese de contar con los siguientes recursos:

* **Software:** [PSeInt](https://pseint.sourceforge.net/) (Compatible con perfiles Flexibles y Estrictos).
* **Hardware de Desarrollo:** Computador portátil HP Victus / Arquitectura x64.
* **Configuración de Idioma:** Español latinoamericano.

---

## 💻 Código Fuente en PSeInt

Para utilizar el código en su entorno local, cree un nuevo archivo en PSeInt, configure el perfil en modo **Flexible** y pegue el siguiente pseudocódigo:

```pseint
Algoritmo AplicativoInteractivo2
	// Constante academica para definir el limite minimo de aprobacion
	Definir NOTA_MINIMA_APROBACION Como Real
	NOTA_MINIMA_APROBACION <- 7.0
	
	// Variables globales de control y datos
	Definir opcion Como Entero
	Definir nombreEstudiante, lenguajeUtilizado Como Cadena
	Definir datosProcesados Como Logico
	Definir confirmarSalir Como Entero
	
	// Variables para almacenar los resultados del sistema
	Definir num1, num2, suma, resta, multiplicacion, division, promedio, notaMayor, notaMenor Como Real
	Definir aprobados, reprobados Como Entero
	Definir banderaOperaciones, banderaNotas Como Logico
