# Actividad: Propuesta de Práctica Temática Pequeña (Enfoque en Documentación)

## 1) Título de la práctica

**Diseño de Propuesta: Mini Proyecto en Terminal con ARM64, C, Python o Bash**

> Puedes personalizar el nombre final de tu práctica. Ejemplos válidos:
> - **Mini Toolkit en ARM64**
> - **Asistente de Estudio en Terminal**
> - **Reporteador de Información del Sistema**
> - **Organizador de Archivos**
> - **Juego de Aprendizaje en Línea de Comandos**

---

## 2) Descripción General

En esta actividad, **no vas a construir un proyecto grande**, sino a **diseñar y documentar una propuesta de práctica temática pequeña** que después pueda implementarse de forma gradual.

Tu propuesta debe:

- Elegir **un lenguaje principal**:
  - **ARM64 Assembly**
  - **C**
  - **Python**
  - **Bash**
- Explicar un caso de uso realista y pequeño que pueda correrse en ambiente local.
- Priorizar la **documentación, planeación y justificación técnica** antes de escribir mucho código.

> **Nota importante sobre ARM64 Assembly:** úsalo solo si tu propuesta es **muy pequeña** (por ejemplo: operaciones aritméticas básicas, manejo simple de entrada/salida o procesamiento mínimo de texto), debido al nivel de detalle del lenguaje.

### Restricciones de alcance (obligatorias)

Para mantener la práctica viable con herramientas gratuitas (Codex u otras IAs con límite):

- Mantén el proyecto **pequeño y acotado**.
- Evita:
  - Frameworks grandes
  - APIs pagadas
  - Bases de datos
  - Servicios en la nube
  - Contenedores
  - Dependencias complejas

---

## 3) Entregables del Estudiante

Tu repositorio debe incluir, como mínimo, los siguientes archivos:

- `README.md`
- `docs/propuesta.md`
- `docs/caso_de_uso.md`
- `docs/estructura_repositorio.md`
- `docs/plan_de_pruebas.md`

Opcionales (si decides avanzar con implementación mínima):

- `src/`
- `scripts/`
- `tests/`

### Contenido esperado por archivo

#### `README.md`
Incluye:
- Nombre de la práctica.
- Lenguaje elegido y justificación breve.
- Objetivo general (1 párrafo).
- Lista de entregables.
- Instrucciones básicas para revisar la documentación.

#### `docs/propuesta.md`
Incluye:
- Problema que quieres atender.
- Objetivo técnico.
- Alcance (qué sí harás y qué no harás).
- Lenguaje principal y por qué.
- Complejidad estimada (baja/media) y razones.
- Plan mínimo de implementación (si aplica).

#### `docs/caso_de_uso.md`
Incluye:
- Contexto del usuario (quién lo usaría).
- Escenario de uso paso a paso.
- Entradas esperadas.
- Salidas esperadas.
- Ejemplo concreto de ejecución o interacción.

#### `docs/estructura_repositorio.md`
Incluye:
- Árbol del repositorio.
- Descripción del propósito de cada carpeta/archivo.
- Convenciones de nombres (archivos, scripts, pruebas).

#### `docs/plan_de_pruebas.md`
Incluye:
- Objetivo de pruebas.
- Casos de prueba mínimos (al menos 5).
- Para cada caso: entrada, procedimiento, resultado esperado.
- Criterios de aceptación.

---

## 4) Estructura Recomendada del Repositorio

Usa esta estructura mínima como base:

```text
nombre-del-proyecto/
├── README.md
├── docs/
│   ├── propuesta.md
│   ├── caso_de_uso.md
│   ├── estructura_repositorio.md
│   └── plan_de_pruebas.md
├── src/
│   └── main.<ext>
├── scripts/
│   └── run.sh
└── tests/
    └── test_plan.md
```

> Donde `<ext>` depende del lenguaje elegido: `s` (Assembly), `c`, `py` o `sh`.

---

## 5) Reglas de Diseño de la Propuesta

1. El proyecto debe resolverse en una escala de práctica corta.
2. La documentación debe permitir que otra persona entienda y continúe el trabajo.
3. Debes justificar decisiones técnicas, no solo listar archivos.
4. Si incluyes código, debe ser **mínimo** y coherente con la propuesta.
5. Tu propuesta debe ser ejecutable en un entorno local estándar (Linux/macOS) sin configuración pesada.

---

## 6) Rúbrica de Evaluación (100 puntos)

- **Claridad de la propuesta (25 pts)**
  - Objetivo claro, alcance delimitado y viabilidad.
- **Calidad del caso de uso (20 pts)**
  - Escenario realista, entradas/salidas definidas.
- **Estructura del repositorio (20 pts)**
  - Organización coherente, nombres claros, navegación sencilla.
- **Plan de pruebas (20 pts)**
  - Casos suficientes, medibles y con resultados esperados.
- **Comunicación técnica en README y docs (15 pts)**
  - Redacción clara, directa, consistente y sin ambigüedades.

---

## 7) Checklist de Entrega

Antes de enviar, verifica:

- [ ] Elegí un lenguaje principal (ARM64 Assembly, C, Python o Bash).
- [ ] Mi propuesta está enfocada en un proyecto pequeño.
- [ ] Incluí todos los archivos obligatorios en `docs/`.
- [ ] Definí alcance y restricciones claras.
- [ ] Incluí al menos 5 casos de prueba con resultado esperado.
- [ ] La estructura del repositorio coincide con la recomendada.
- [ ] Mi documentación permite entender el proyecto sin explicación oral adicional.

---

## 8) Sugerencias de Temas Pequeños (opcionales)

- Conversor simple de unidades en terminal.
- Organizador de archivos por extensión.
- Generador de recordatorios en texto plano.
- Reporte básico de uso del sistema (CPU/RAM/disco) con comandos locales.
- Mini quiz de comandos de Linux.

---

## 9) Formato de Entrega en GitHub Classroom

- Repositorio individual por estudiante.
- Commits con mensajes descriptivos (ej. `docs: define alcance de la propuesta`).
- Entrega final en la rama principal del repositorio asignado.

---

## 10) Resultado Esperado

Al finalizar, debes tener una **propuesta sólida, bien documentada y viable** de una práctica temática pequeña. Esta propuesta debe servir como base para una implementación posterior sin depender de infraestructura compleja.
