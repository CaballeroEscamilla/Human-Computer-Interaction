# Requisitos No Funcionales

### Usabilidad 

   - **RNF-1:** El sistema debe permitir la consulta y actualización de expedientes en un tiempo máximo de 5 minutos, medido desde el inicio de la sesión hasta la confirmación del cambio. 

   - **RNF-2:** La interfaz debe ser intuitiva para nuevos usuarios, con un tiempo de aprendizaje menor a 2 días. Se logrará mediante: 

      - Un tutorial interactivo en el primer acceso. 

      - Un sistema de ayuda contextual con instrucciones específicas según la sección. 

      - Indicaciones visuales para errores o acciones incompletas. 

   - **RNF-3:** La organización de la información debe seguir una jerarquía clara: 

      - Datos personales del paciente en la parte superior. 

      - Historial clínico accesible en pestañas o secciones colapsables. 

      - Opciones de acción destacadas con colores diferenciados (ejemplo: verde para confirmar, rojo para eliminar). 

### Seguridad 

   - **RNF-4:** Se debe asegurar la confidencialidad de la información de los pacientes mediante un nivel de seguridad que cumpla con estándares de cifrado de al menos AES-256 en la base de datos 

   - **RNF-5:** Se debe aplicar control de acceso basado en roles (RBAC), asegurando que cada usuario solo pueda acceder a la información necesaria según su función. 

   - **RNF-6:** El sistema debe cumplir con normativas éticas y legales de confidencialidad, como la Ley General de Protección de Datos Personales en Posesión de Sujetos Obligados (LGPDPPSO) y Normas ISO/IEC 27001 en gestión de seguridad de la información. 

   - **RNF-7:** El sistema debe garantizar la seguridad de las sesiones de usuario mediante la protección contra accesos no autorizados. En caso de inactividad de más de 15 minutos, el sistema cerrará la sesión automáticamente y requerirá reautenticación. 

### Rendimiento 

   - **RNF-8:** El sistema debe ser capaz de gestionar múltiples consultas simultáneamente sin degradar la experiencia del usuario, optimizando la ejecución de consultas a la base de datos. 

   - **RNF-9:** El tiempo de respuesta en la carga y consulta de expedientes no debe exceder los 2 segundos en condiciones normales de operación. 

   - **RNF-10:** El sistema debe soportar el acceso concurrente de múltiples usuarios sin afectar la velocidad de procesamiento. 

   - **RNF-11:** Se debe utilizar una arquitectura escalable con balanceo de carga que permita soportar la demanda de las consultas. 

### Portabilidad 

RNF-12: El sistema debe ser accesible desde dispositivos móviles y computadoras, asegurando una experiencia fluida en diferentes resoluciones de pantalla. 

RNF-13: Debe ser compatible con múltiples navegadores web, asegurando una experiencia fluida en diferentes resoluciones de pantalla. 

RNF-14: El diseño debe ser responsivo: 

Elementos ajustables según la pantalla (ejemplo: menús desplegables en móviles). 

Bot14ones de acción con un tamaño mínimo de 44x44 píxeles en dispositivos táctiles. 

Tipografía legible con un tamaño mínimo de 16px. 

Mantenibilidad 

RNF-15: El sistema debe proveer una de digitalización de documentos físicos eficiente y fácil de usar, con compatibilidad para escáneres y OCR, reduciendo el tiempo de procesamiento a un promedio de 2 minutos por documento. 

RNF-16: El código debe estar bien documentado y seguir estándares de desarrollo que faciliten futuras modificaciones o ampliaciones del sistema como el Javadoc. 

RNF-17: Se implementará una arquitectura modular que permita: 

La adición de nuevos módulos sin afectar el rendimiento. 

La actualización independiente de cada módulo sin afectar a otros. 

Confiabilidad 

RNF-18: El sistema debe estar disponible al menos el 99.9% del tiempo en horarios de uso frecuente (lunes a viernes de 9:00 - 15:00 horas), para garantizar la continuidad del servicio. 

RNF-19: El sistema debe tener una alta confiabilidad y tolerancia a fallos, asegurando que no se pierda información en caso de errores, y con un tiempo de recuperación inferior a 10 minutos. 

RNF-20: Debe contar con mecanismos de respaldo automático como Copia de seguridad y Restauración de datos en caso de falla crítica. 