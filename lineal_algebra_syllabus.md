# Syllabus: Álgebra Lineal para IA y Machine Learning

## Requisitos previos
- Álgebra básica (ecuaciones, funciones).
- Cálculo diferencial básico (derivadas de una variable).  
  *La parte multivariable la veremos más adelante en notación matricial.*

---

## Módulo 0 — Fundamentos y notación (1 semana)
**Objetivos**
- Manejar con soltura la notación de vectores/matrices.
- Entender qué representan en datos y modelos.

**Temas**
- Escalares, vectores, matrices, tensores (idea general).
- Dimensiones y *shape*.
- Transpuesta.
- Convenciones en ML:  
  - dataset \(X \in \mathbb{R}^{n \times d}\)  
  - targets \(y \in \mathbb{R}^{n}\)  
  - pesos \(w \in \mathbb{R}^{d}\)

**Práctica**
- Identificar *shapes* en ejemplos reales.
- Traducir problemas de texto a notación matricial.

---

## Módulo 1 — Operaciones básicas de vectores y matrices (1 semana)
**Objetivos**
- Operar correctamente y entender el significado geométrico.

**Temas**
- Suma/resta, producto por escalar.
- Producto punto (dot product) y propiedades:
  - simetría, distributividad.
- Producto matricial:
  - compatibilidad de dimensiones.
  - interpretación como combinaciones lineales.
- Matriz identidad y matrices diagonales.

**Práctica**
- Hacer multiplicación matricial a mano y en Python.
- Ejercicios de interpretación geométrica del dot product.

---

## Módulo 2 — Normas, distancias y similitud (1 semana)
**Objetivos**
- Interpretar “tamaño” y “parecido” entre datos.

**Temas**
- Norma L1, L2, infinito.
- Distancias métricas: Euclídea, Manhattan.
- Similaridad coseno:
  \[
  \cos(\theta)=\frac{x\cdot y}{||x||\,||y||}
  \]
- Desigualdad de Cauchy–Schwarz (intuición).

**Aplicaciones ML**
- KNN, clustering, embeddings, recomendadores.

**Práctica**
- Comparar métricas en datos simples.
- Observar cómo cambia KNN usando distintas normas.

---

## Módulo 3 — Sistemas de ecuaciones lineales (1–1.5 semanas)
**Objetivos**
- Resolver \(Ax=b\) y entender tipos de solución.

**Temas**
- Sistemas lineales: interpretación geométrica.
- Eliminación Gaussiana y RREF.
- Tipos de solución:
  - única, infinitas, ninguna.
- Matriz inversa: existencia y significado.

**Aplicaciones ML**
- Regresión lineal vista como sistema.

**Práctica**
- Resolver sistemas con Gauss.
- Detectar singularidad y explicarla.

---

## Módulo 4 — Espacios vectoriales y subespacios (1 semana)
**Objetivos**
- Entender el espacio donde viven los datos.

**Temas**
- Espacio vectorial y subespacio.
- Combinación lineal y *span*.
- Independencia lineal.
- Base y dimensión.
- Rango (*rank*) y nulidad (*nullity*).
- Teorema rango–nulidad.

**Aplicaciones ML**
- Features redundantes, colinealidad.
- Compresión/reducción de dimensión.

**Práctica**
- Hallar bases y dimensiones.
- Interpretar rank en datasets reales.

---

## Módulo 5 — Ortogonalidad y proyecciones (1 semana)
**Objetivos**
- Dominar la idea clave detrás de mínimos cuadrados y PCA.

**Temas**
- Ortogonalidad y ortonormalidad.
- Proyección sobre un vector y sobre un subespacio.
- Matrices ortogonales.
- Gram–Schmidt.

**Aplicaciones ML**
- **Regresión lineal = proyección**.
- PCA como proyección a un mejor subespacio.

**Práctica**
- Proyecciones a mano.
- Ortonormalización con Gram–Schmidt.

---

## Módulo 6 — Mínimos cuadrados y regresión lineal (1 semana)
**Objetivos**
- Conectar álgebra lineal con un modelo real.

**Temas**
- Problema:
  \[
  \min_w ||Xw-y||^2
  \]
- Ecuaciones normales:
  \[
  X^T X w = X^T y
  \]
- Condiciones de existencia y unicidad.
- Regularización Ridge:
  \[
  \min_w ||Xw-y||^2 + \lambda ||w||^2
  \]

**Aplicaciones ML**
- Modelo base de ML clásico.

**Práctica**
- Derivar ecuaciones normales.
- Resolver regresión con y sin regularización.

---

## Módulo 7 — Eigenvalores y eigenvectores (1–1.5 semanas)
**Objetivos**
- Entender direcciones “especiales” del espacio.

**Temas**
- Definición:
  \[
  Av=\lambda v
  \]
- Cálculo de eigenvalores y eigenvectores.
- Diagonalización y multiplicidad.
- Interpretación geométrica.

**Aplicaciones ML**
- Covarianza → PCA.
- Estabilidad de optimización.

**Práctica**
- Hallar eigenvalores/eigenvectores.
- Interpretar espectro de matrices simples.

---

## Módulo 8 — Descomposiciones matriciales (1 semana)
**Objetivos**
- Manejar herramientas numéricas clave.

**Temas**
- Diagonalización \(A=PDP^{-1}\).
- SVD:
  \[
  X = U\Sigma V^T
  \]
- Relación SVD ↔ PCA.
- Interpretación de valores singulares.

**Aplicaciones ML**
- PCA práctico.
- Compresión, denoising, embeddings.

**Práctica**
- Implementar PCA con SVD.
- Reconstrucciones aproximadas con k valores singulares.

---

## Módulo 9 — Optimización en notación matricial (1 semana)
**Objetivos**
- Leer deep learning con lenguaje lineal.

**Temas**
- Gradiente como vector.
- Jacobiano y Hessiano (idea).
- Derivadas típicas:
  - \(\nabla_w ||Xw-y||^2\)
  - \(\nabla_w (w^T w)\)
- Regla de la cadena en forma matricial.

**Aplicaciones ML**
- Descenso por gradiente.
- Base de backprop.

**Práctica**
- Derivar gradientes de pérdidas comunes.
- Implementar GD para regresión lineal.

---

## Módulo 10 — Temas extra para ML avanzado (opcional)
**Objetivos**
- Prepararte para papers modernos.

**Temas**
- Formas cuadráticas \(x^T A x\).
- Matrices definidas positivas/semidefinidas.
- Condicionamiento numérico.
- Traza y determinante en ML.
- Convoluciones como operaciones lineales (idea).

**Aplicaciones**
- Kernel methods, Gaussian Processes, métodos de 2º orden.

---

## Evaluación sugerida
- **Quizzes cortos (20%)**: shapes, operaciones, conceptos.
- **Problem sets (40%)**: ejercicios por módulo.
- **Proyecto final (40%)**:
  - Implementar PCA y regresión lineal desde cero.
  - Explicar matemáticamente qué pasa.
  - Comparar contra librerías.

---

## Proyecto final propuesto
**Título:** “De datos crudos a modelo interpretable”

1. Cargar un dataset real (housing, iris, MNIST reducido, etc.).
2. Estandarizar y analizar rank/colinealidad.
3. Aplicar PCA con SVD (elige k).
4. Entrenar regresión lineal o ridge en el espacio reducido.
5. Reportar:
   - varianza explicada,
   - error antes/después de PCA,
   - interpretación geométrica.

---

## Checklist de dominio
- [ ] Identificas shapes sin esfuerzo.
- [ ] Explicas \( \hat{y}=Xw \) en palabras y geometría.
- [ ] Entiendes mínimos cuadrados como proyección.
- [ ] Haces PCA con eigen o SVD y lo interpretas.
- [ ] Derivas gradientes básicos en notación matricial.
