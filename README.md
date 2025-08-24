🧠 Demo de Razonamiento con Gemini (Chain-of-Thought)
* 🧩 Chain-of-Thought (CoT) Sample
* 🎯 Zero-Shot con razonamiento guiado
* 🔁 Self-Consistency (múltiples muestreos y selección)

### Importante (ética y producción): evitar solicitar o mostrar razonamientos paso a paso completos en entornos de producción. Prefiere respuestas concisas y verificables (p. ej., “da el resultado y un breve resumen del procedimiento”).

🚀 ¿Qué hace esta demo?
- Configura Gemini 1.5 Pro via google-generativeai.
- Ejecuta tres estilos de prompting para observar diferencias en las respuestas:
  * CoT Sample: guía al modelo con “pensemos paso a paso”.
  * Zero-Shot: resuelve sin ejemplos, con una breve instrucción de razonamiento.
  * Self-Consistency: genera varias respuestas y compara resultados (útil para reducir errores por muestreo).

🛠️ Tecnologías
- Python 3.9+
- Google Generative AI (Gemini 1.5 Pro)ç
- IPython.display (Markdown) para formatear salidas en cuadernos

⚙️ Requisitos previos
- Cuenta y API Key de Google Generative AI.
- Entorno tipo Jupyter o Google Colab.

🧪 Flujos incluidos
- Chain-of-Thought – Sample: guía explícitamente a la reflexión.
- Chain-of-Thought – Zero-Shot: instrucción mínima con razonamiento breve.
- Self-Consistency: ejecuta varias generaciones y (opcional) agrega una regla simple de votación por mayoría para el resultado final.

🧭 Buenas prácticas
- En producción, usa respuestas breves y evita reproducir cadenas de pensamiento completas.
- Considera agregar verificación programática de resultados (p. ej., recalcular operaciones) cuando sea posible.
- Limita parámetros de salida (tokens) y controla temperatura/top-p según caso de uso.

▶️ Uso
- Configura la API Key en el entorno.
- Abre el notebook o script de la demo.
- Ejecuta los tres enfoques (Sample, Zero-Shot, Self-Consistency) y compara resultados.

### (Opcional) Implementa una votación por mayoría para Self-Consistency.

⚠️ Limitaciones
- Los modelos generativos pueden cometer errores en aritmética si los prompts o parámetros no están calibrados.
- Self-Consistency incrementa el costo porque realiza múltiples generaciones.
- Evita exponer razonamientos largos al usuario final; prioriza respuestas verificables.
