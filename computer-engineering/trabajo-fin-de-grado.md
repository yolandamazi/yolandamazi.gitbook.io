---
description: >-
  Actualmente estoy trabajando y redactando mi TFG, por lo que usaré este
  espacio para documentar tanto la investigación como el desarrollo de este.
hidden: true
---

# Trabajo Fin de Grado

## — ¿cómo inicio?

### 1. El título, mejor conocido como el tema

Para poder crear un primer esqueleto, he querido empezar eligiendo un buen título, es decir, el tema. Estoy dubitativa entre varios temas, aunque me decanto principalmente en ciberinteligencia y credenciales expuestas. Actualmente tengo dos opciones:

* Ciberinteligencia para el tratamiento operativo de credenciales expuestas: diseño e implementación de una herramienta para la identificación temprana, evaluación del riesgo y priorización en respuesta a incidentes
* Análisis de credenciales expuestas mediante ciberinteligencia: herramientas para la identificación temprana y priorización de riesgos en incidentes de seguridad

Como puedes haberte dado cuenta, ambos tratan del mismo tema, mirándolo en rasgos generales. Busco relacionar la ciberinteligencia con una herramienta web desarrollada para detectar credenciales expuestas (leaks), integrándola dentro de la gestión de riesgos en la respuesta a incidentes TIC y la continuidad del negocio, que es el área en la que actualmente trabajo. Me decanto más por la primera ya que da un primero boceto general del tema y luego desarrolla m'as el tema.

### 2. Índice: capítulos y secciones

Para desarrollar el esqueleto que mencionaba anteriormente, contar con un índice predefinido me permite conocer el camino que quiero seguir durante el desarrollo del tfg. Como primer boceto tengo esta idea:

1. Introducción
   1. Contexto y relevancia del problema
      1. Historia y evolución de incidentes relacionados con credenciales expuestas.
      2. Impacto económico, operativo y reputacional.
   2. Objetivos del TFG
      1. Generales
      2. Específicos, detallando la aplicación práctica en IR.
   3. Alcance y limitaciones
      1. Qué incluye y qué no, incluyendo límites de simulaciones y datos.
   4. Metodología general
      1. Explicación de la combinación ciberinteligencia + desarrollo web + IR profesional.
2. Marco conceptual
   1. Ciberinteligencia: definición, ciclo y procesos
   2. Credenciales expuestas: tipologías, fuentes de información y riesgos
   3. Gestión de incidentes de seguridad
      1. Tipos de incidentes relacionados con credenciales
      2. Ciclo de vida de un incidente
   4. Priorización de riesgos en seguridad
      1. Conceptos de scoring, matrices, likelihood e impacto
   5. Frameworks y buenas prácticas de IR
      1. NIST, MITRE ATT\&CK, ISO 27001, etc.
   6. Integración de ciberinteligencia en IR
      1. Cómo la inteligencia transforma datos en decisiones
3. Desarrollo de la herramienta web
   1. Arquitectura general y tecnologías empleadas
      1. Diagrama de arquitectura y flujo de datos
   2. Backend: cálculo de riesgos y scoring automático
      1. Explicación de fórmulas y lógica
      2. Fragmentos de código comentados
   3. Frontend: dashboard interactivo y visualización de prioridades
      1. Capturas, gráficos y heatmaps
      2. Explicación de cada widget y su valor para IR
   4. Funcionalidades: filtrado, alertas, reportes
   5. Integración de la herramienta en el flujo de priorización de incidentes
      1. Ejemplo paso a paso de cómo un analista usaría la herramienta
4. Priorización de riesgos en incidentes de seguridad
   1. Cómo usar la herramienta para priorizar incidentes
   2. Modelos de scoring y matrices de riesgo
      1. Explicación detallada de criterios de impacto y probabilidad
   3. Identificación temprana de incidentes críticos
   4. Metodología para priorizar acciones y recursos
      1. Ejemplos prácticos basados en tu experiencia profesional
   5. Incorporación de playbooks
      1. Acciones a seguir
5. Validación y escenarios de prueba
   1. Casos de prueba simulados (table-top / escenarios ficticios)
   2. Aplicación de la herramienta para priorizar incidentes
   3. Análisis de resultados: cómo cambia la respuesta según la priorización
   4. Lecciones aprendidas y mejora de playbooks
6. Discusión
   1. Valor de la herramienta para ciberinteligencia y priorización de riesgos
   2. Comparación con frameworks y metodologías de IR existentes
   3. Limitaciones técnicas y operativas
   4. Posibles extensiones futuras
7. Conclusiones y recomendaciones
   1. Conclusiones generales
   2. Recomendaciones para equipos de incident response y gestión de crisis
   3. Aplicabilidad de la metodología y la herramienta en entornos reales
8. Bibliografía
9. Anexos
   1. Código de la herramienta web
   2. Tablas de datos simulados y scoring
   3. Diagramas de flujo, dashboard y playbooks
   4. Resumen de escenarios de crisis y table-tops

Simplemente le pedí, al tool que todos usamos obviamente (la IA), que me generara una primera idea del índice, aunque seguramente le implemente mejoras y cambios.

### 3. Lenguajes y frameworks

Como ya os habreis dado cuenta, para este trabajo debo programar, por tanto debo elegir los lenguajes y frameworks que usaré para la herramienta a desarrollar. Cabe recalcar que esta es mi primera vez programando web, pero mi intención es que a medida que avance, desarrollar esos conocimientos en desarrollo web que todavía no tengo. Digamos que es una especie de learning 2x1.
