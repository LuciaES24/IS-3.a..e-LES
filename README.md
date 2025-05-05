# IS-3.a..e-LES

# Resumen Unidad 3: Investigación de incidentes

## 3.1 Recopiación y almacenamiento de evidencias

### Recopilación de evidencias

+ **Evidencias**: Son los datos que se recopilan durante la investigación de un incidente de seguridad. Estos pueden ser de distinto tipo y procedencia.

+ **Recopilación de evidencias**: Es un proceso crítico en la gestión de incidentes de seguridad. La integridad, autenticidad y admisibilidad de la evidencia son fundamentales para garantizar que los resultados de la investigación sean válidos y puedan ser utilizados en un juicio.

La anticipación y el entrenamiento previo son clave para gestionar las evidencias y para ello existen tres pilares que se deben tener en cuenta para ello:

+ Personas.
+ Procedimientos.
+ Herramientas.

### Metodología de recopilación y almacenamiento

+ **Preservación**: mantener la integridad de la evidencia.
+ **Adquisición**: recoger la evidencia de forma que sea admitida en un juicio.
+ **Documentación**: documentar el proceso de recogida de evidencias. Debe ser preciso y detallado.
+ **Análisis**: analizar la evidencia de forma imparcial, con el objetivo de extraer información.
+ **Presentación**: presentar la evidencia de forma clara y comprensible.

La guía por excelencia que proporciona pautar para la recopilación y almacenamiento de evidencias digitales es la **RFC 3227**.

### RFC 3227

Es un documento que recoge las directrices para la recopilación de evidencias y su almacenamiento.

#### Principios

+ Realizar la captura del sistema lo más preciosa posible.
+ Realizar anotaciones detalladas, incluyendo fechas y horas.
+ Minimizar los cambios en la información para asegurar su integridad.
+ Realizar primero la recolección y posteriormente el análisis de las evidencias.
+ Tener en cuenta el orden de volatilidad.
+ Tener en cuenta el tipo de dispositivo para recoger la información.

El **orden de volatilidad** es el periodo de tiempo en el que está accesible cierta información. Para ello existe un orden:
+ Registros y contenido de la caché
+ Tabla de enrutamiento, caché ARP, tabla de procesos, estadísticas del kernel, memoria.
+ Información temporal del sistema.
+ Disco.
+ Logs del sistema.
+ Configuración física y topología de la red.
+ Documentos.

Cosas que **NO** se deben hacer:
+ Apagar el ordenador.
+ Ejecutar programas que modifiquen la fecha y la hora de acceso de los ficheros.
+ Confiar en la información proporcionada por los programas del sistema ya que pueden haberse modificado.
+ Utilizar el sistema comprometido para recopilar la información.

En cuanto a la **privacidad** deben tenerse en cuenta algunos aspectos:
+ Tener en consideración las pautas de la empresa en cuanto a la privacidad.
+ No hay que entrometerse en la privacidad de las personas sin justificación.
+ No recopilar datos de lugares a los que normalmente no hay razón para acceder.

#### Procedimiento de recolección

El método utilizado para recolectar evidencias debe de ser transparente y reproducible. La información debe ser relevante y suficiente.

Pasos:
1. Listar sistemas involucrados y de cuáles se van a tomar evidencias.
2. Establecer qué es relevante.
3. Fijar el orden de volatilidad.
4. Obtener la información en el orden establecido.
5. Comprobar la sincronización del reloj del sistema.
6. Documentar los pasos.
7. Tomar notas sobre qué gente estaba allí, qué estaban haciendo, qué observaron y cómo reaccionaron.

#### Procedimiento de almacenado

La evidencia debe ser almacenada de forma segura para garantizar su integridad y autenticidad.

Se debe tener en cuenta la cadena de custodia, en la que hay que incluir:
+ ¿Dónde?, ¿cuándo? y ¿quién? descubrió y recolectó la evidencia.
+ ¿Dónde?, ¿cuándo? y ¿quién? manejó la evidencia.
+ ¿Quién ha custodiado la evidencia?, ¿cuánto tiempo? y ¿cómo la ha almacenado?.
+ En el caso de que la evidencia cambie de custodia indicar cuándo y cómo se realizó el intercambio, incluyendo número de albarán, etc.

Además, se debe saber dónde y cómo almacenar la información, demostrando la seguridad del tipo de almacenamiento, garantizando la integridad y permitiendo el acceso solo al personal autorizado, detectando intrusos en el caso de intentos de acceso no autorizado.

#### Herramientas

Algunas pautas que proporciona la RFC 3227 sobre las herramientas:
+ Herramientas externas al sistema, para evitar que hayan podido ser comprometidas.
+ Herramientas que alteren lo mínimo posible el escenario (no GUI, evitar uso excesivo de memoria).
+ Deben estar ubicados en un dispositivo de solo lectura. (CDROM, USB).
+ Tener un kit básico de herramientas según S.O, que incluyan:
+ Listar y examinar procesos.
+ Examinar el estado del sistema.
+ Realizar copias bit a bit.

## 3.2 Guía y procedimiento para la recopilación y almacenamiento de evidencias digitales

Es un proceso crítico en el ámbito de la seguridad informática y la investigación forense. A continuación se presenta una guía para llevar a cabo estos procedimientos.

### Objetivo

Asegurar que la evidencia digital se recopile y almacene de manera segura, preservando su integridad, autenticidad y cadena de custodia, para su posterior análisis.

### Fase 1: Preparación para la recopilación

#### 1. Conocimiento y autorización

+ Definir el alcance de la investigación y los objetivos.
+ Verificar la autoridad legar para la recopilación.
+ Autorizar sólo al personal necesario.

#### 2. Herramientas

+ Preparar un kit de herramientas forenses.
+ Dispositivos de bloqueo de escritura.
+ Dispositivos para crear copias forenses/imágenes.
+ Utilizar medios de almacenamiento limpios.
+ Herramientas de hashes.
+ Etiquetas de evidencia.
+ Bolsas antiestáticas.
+ Cámara de foto o video.
+ Cadena de custodia.
+ Bloc de notas y bolígrafo.

#### 3. Personal

Se debe asignar al personal autorizado capacitado para realizar la investigación forense. Además, se puede considerar tener testigos independientes para dar fé del proceso.

#### 4. Planificación previa a la escena

+ Revisar los procedimientos predefinidos del laboratorio. Tener un plan de acción.
+ Tener en cuenta las directrices policiales locales.
+ Contar con personal con formación especializada en el caso de que haya equipos informáticos especializados.

### Fase 2: Recopilación de evidencia en la escena

#### 1. Aseguramiento y documentación de la escena:

+ Aislar la escena.
+ Documentar detalladamente la escena, teniendo en cuenta hacer un croquis de la escena, anotar los detalles de las personas presentes, realizar fotografías o videos y tomar notas en el momento de todas las observaciones.

#### 2. Identificación y manejo de dispositivos

+ Identificar los dispositivos.
+ Etiquetar cada dispositivo y su cableado.
+ No encender dispositivos apagados ni apagar dispositivos encendidos.
+ Documentar lo que esté en la pantalla de los dispositivos encendidos.
+ Buscar notas, diarios o documentos cercanos a los dispositivos que puedas contener información relevante.

#### 3. Preservación de la evidencia durante la repocilación

+ Manipular los dispositivos con precaución.
+ Proteger la evidencia de campos magnéticos, descargas electrostáticas, y condiciones ambientales extremas.
+ Si se desconecta un dispositivo de la fuente de alimentación, ser consciente de la posible pérdida de datos volátiles y de la limitada vida de las baterías.
+ Considerar el aislamiento de la red para evitar alteraciones remotas.

#### 4. Adquisición de evidencia en la escena

+ Utilizar dispositivos de bloqueo de escritura.
+ Crear una copia forense utilizando herramientas válidas.
+ Calcular el hash original antes de la copia y posteriormente el de esta para comparar.

#### 5. Embalaje y transporte

+ Embalar la copia de la evidencia de forma segura.
+ Utilizar bolsas antiestáticas.
+ Evitar doblar, golpear o exponer la evidencia.
+ Mantener la evidencia alejada de fuentes magnéticas.
+ Documentar el embalaje.

### Fase 3: Akmacenamiento seguro de la evidencia

#### 1. Recepción y registro en el laboratorio

+ Verificar la integridad del embalaje y documentar su estado.
+ Registrar formalmente la recepción en la cadena de custodia.
+ Realizar una evaluación inicial.

#### 2. Almacenamiento físico

+ Elegir un lugar seguro con acceso restringido y controlado.
+ Proteger la evidencia de factores ambientales.
+ Utilizar armarios o cajas fuertes.
+ Mantener el inventario actualizado.

#### 3. Almacenamiento digital

+ Deben almacenarse el medios seguros y fiables, utilizando discos cifrados y control de acceso por contraseña.
+ Implementar contoles de acceso.
+ Realizar copias de seguridad.
+ Mantener un registro de acceso.
+ Considerar la obsolencia de los medios almacenados.

#### 4. Mantenimiento de la cadena de custodia

+ Documentar cada movimiento o manupulación de la evidencia.
+ Utilizar formularios de cadena de custodia.
+ Asegurar que cada persona que manipula la evidencia firme y feche el formulario de cadena de custodia.

### Fase 4: Disposición final de la evidencia

+ La evidencia debe ser devuelta a su propietario o eliminada de forma segura una vez finalizado el análisis.
+ Documentar la disposición final en la cadena de custodia.

## 3.3 Investigación de incidentes: MITRE

### Matriz Att&ck 

Permite investigar un incidente desde el punto de vista de un atacante. Algunas características básicas:
+ **Tácticas**: Son los métodos o fases para alcanzar un objetivo específico.
+ **Técnicas**: Son las formas en que se pueden llevar a cabo las tácticas para alcanzar los objetivos definidos en estas últimas.
+ **Mitigación**: Son las formas en que se pueden mitigar las técnicas.
+ **APT (Advanced Persistent Threat)**: Son los grupos de actores de amenazas que utilizan las tácticas y técnicas, como APT28, APT29, APT30, etc. Son grupos de ciberdelincuentes que se dedican a realizar ciberataques de forma organizada y con un objetivo concreto.
+ **Software**: Son los programas maliciosos que utilizan las tácticas y técnicas.

Existe el navegador Mitre Att&ck el cual es una hoja interactiva que permite enfocar y pririzar ciertos puntos clave dependiendo de la infraestructura.

Algunos sectores en los que Att&ck es útil:
+ Inteligencia de amenazas.
+ Detección y análisis de ataques.
+ Emulación del adversario y formación de red team.
+ Evaluaciones e ingeniería.

### Matriz Re&ct

Al contrario que Att&ck, permite investigar un incidente desde el punto de vista de la defensa. Esta puede utilizarse para la identificación de brechas de seguridad o mejorar las capacidades de respuesta a incidentes. Esta matriz consta de seis etapas:

+ **Preparación**: Hay que encargarse de preparar todo lo necesario para poder realizar un proceso de respuesta a incidentes de forma adecuada.
+ **Identificación**: Se encuentran acciones a emprender que nos ayudarán a iniciar esta fase.
+ **Contención**: Es de las fases a la que más valor se le suele dar, pero no se puede sin haber realizado las etapas anteriores.
+ **Erradicación**: En esta etapa se eliminan las vulnerabilidades o rastros que haya dejado el atacante que pueda hacer que el sistema siga siendo vulnerable.
+ **Recuperación**: Se vuelven a poner en marcha los sistemas una vez están listos.
+ **Lecciones aprendidas**: A partir de los sucesos y los pasos llevados a cabo durante el incidente, se toman unas pautas sobre los pasos que han sido positivos y negativos durante la defensa.

Al igual que con Att&ck existe un navegador interactivo, con las técnicas enumeradas en cada fase. Este proyecto es muy ambicioso ya que comtempla la recopilación de playbooks.
