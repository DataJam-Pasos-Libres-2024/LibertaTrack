# DataJam Pasos Libres 2024 – LibertaTrack

Este es un repositorio de proyectos de investigación en el ámbito de la esclavitud moderna. Incluye todas las ideas de proyectos o temas de investigación que serían útiles para nuestro proyecto.
Esto incluiría lo siguiente:

# Tabla de contenido
0. [Nosotros](#Nosotros)
   1. [¿Quienes somos?](#1-¿Quienes-somos?)
   2. [Motivación para participar en la competencia](#2-Motivacion-para-participar)
1. [Planteamiento del problema](#1-Planteamiento-del-problema)
2. [Objetivo](#Objetivo)
   1. [Objetivo general](#1-objetivo-general)
   2. [Objetivo específico](#2-objetivo-especifico)
3. [Descripción Solución/Caso Uso de Datos](#3-descipcion-solucion/caso-uso-de-datos)
4. [Pitch](#1-Pitch)
5. [Datasets](#Datasets)
6. [Código Proyecto](#Codigo-proyecto)
7. [Documentos Adicionales (Opcional)](#Documentos-adicionales-(opcional))
   1. [Demo de LibertaTrack y Tech Stack](#1-demo-de-libertaTrack-y-tech-stack)
   2. [Pasos para lanzar la infraestructura como código](#2-pasos-para-lanzar-la-infraestructura-como-codigo)
   3. [Instrucciones para ejecutar la aplicación móvil de forma local](#3-instrucciones-para-ejecutar-la-aplicacion-movil-de-forma-local)
   4. [Instrucciones para ejecutar la aplicación web de forma local](#4-instrucciones-para-ejecutar-la-aplicacion-web-de-forma-local)
   5. [Arquitectura de solución del chatbot en AWS](#5-arquitectura-de-solucion-del-chatbot-en-AWS)
   6. [Propuesta de la arquitectura de solución en etapa de producción](#6-propuesta-de-la-arquitectura-de-solucion-en-etapa-de-produccion)
8. [Referencias](#Referencias)

# 0. Nosotros
---
## 0.1. ¿Quienes somos?

Somos un equipo multidisciplinario. Cada integrante aporta habilidades que van desde el desarrollo de software y el análisis de datos, hasta el diseño, marketing y el conocimiento en derechos humanos y justicia social. Abordamos problemas desde múltiples perspectivas para crear soluciones innovadoras. Tenemos sólida experiencia trabajando juntos en proyectos anteriores y promovemos una dinámica de equipo que impulsa la creatividad, inclusión e innovación.

![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/5024d659-e232-40a5-803a-d54877424601)


## 0.2. Motivación para participar en la competencia

Nuestra motivación surge de un compromiso compartido con la justicia social y la convicción de que la tecnología y el análisis de datos pueden ser catalizadores poderosos para el cambio. Juntos, queremos aplicar nuestra pasión y habilidades para contribuir significativamente a la lucha contra la esclavitud moderna. Por tal razón, valoramos profundamente la oportunidad de mentoría y colaboración que la DataJam ofrece. Creemos que aprender de los expertos y colaborar con otros equipos puede potenciar nuestra capacidad para enfrentar los retos planteados y, en consecuencia, fortalecer el impacto de nuestras soluciones. 

Realmente confiamos en que nuestra mezcla única de habilidades, pasión y visión hará una contribución valiosa a la DataJam Pasos Libres. Estamos ansiosos por aportar nuestro entusiasmo y conocimientos en la lucha contra la esclavitud moderna. Además, no nos cabe duda que nuestro equipo no solo cumplirá con las expectativas de la competencia, sino que las excederá, aportando una solución creativa y eficaz.

# 1. Planteamiento del Problema
---
El centro de la DataJam Pasos Libres 2024 y de este documento se encuentra en buscar soluciones a la esclavitud moderna. De acuerdo con el Global Slavery Index 2023 (Walk Free, 2023) es un problema que abarca todos los aspectos de la sociedad, incluyendo la ropa que usamos, nuestros electrodomésticos y los alimentos que consumimos. La esclavitud moderna, es además de todo, una manifestación de una desigualdad extrema. Por su misma complejidad, este flagelo involucra un sinfín de causas tales como la pobreza o la migración forzada, y consecuencias como la explotación infantil, la trata de personas o la explotación
sexual. Así las cosas, se hace necesario acotar el problema a escenarios y procesos específicos. En este caso, se hace énfasis en rol que juegan las empresas y sus cadenas de suministro. Así, algunas consideraciones relevantes para el trazado de los objetivos y el diseño de la solución son: 

a). **La esclavitud moderna es un fenómeno creciente**. De acuerdo con las cifras del Global Slavery Index (2023) en el mundo hay aproximadamente 50 millones de personas en condición de esclavitud moderna, 10 millones más que en la última medición del 2016. De estas, 28 millones tienen trabajos forzados, 22 millones matrimonios forzados y 12 millones son casos de trabajo infantil. Así mismo, según este mismo informe, las acciones estatales son insuficientes alrededor del mundo en tanto los países que llevan la delantera en toma de acciones, no superan el 70% (United Kingdom 68%, Australia y Países Bajos 67%); y los de menor reacción incluso tienen porcentajes negativos (Corea del Norte -3%). 

b) Aunque existen avances en el marco normativo de algunos países como Reino Unido (Ley de Esclavitud Moderna, 2015), Australia (Ley de Esclavitud Moderna, 2018) o Canadá (Ley de lucha contra el trabajo forzoso y el trabajo infantil en las cadenas de suministro, 2023), que exigen a las empresas reportar sus riesgos y acciones contra la esclavitud moderna, son **arreglos normativos que no en todos los casos logran su cometido y, sobre todo, cuyos alcances no tienen incidencia sobre los países más nafectados en Sur América, África o del Sudeste Asiático.**

c) El mercado de trabajo, al menos en el caso colombiano, está sesgado hacia la pequeñez. Según cifras de la Misión de Empleo (Alvarado et al., 2021), **el 97% de las empresas tienen entre 1 a 3 trabajadores** y 81% son informales. Esta última condición de informalidad hace más vulnerables a trabajadores según lo reportado por Walk Free (2023). Además, teniendo en cuenta el tamaño de las empresas, es necesario pensar en estrategias de autodiagnóstico y fortalecimiento de capacidades en torno a la esclavitud moderna que sean accesibles en costos y recursos humanos para las micro y pequeñas empresas. 

d) En la actualidad, **los mercados muestran favoritismo por empresas con prácticas sostenibles, socialmente responsables o de gobernanza**. Según un estudio de reciente de las consultoras McKinsey y NielsenIQ (Frey et al., 2023), los consumidores se preocupan por la sostenibilidad, la responsabilidad social y la gobernanza. Así, 78% de las personas encuestadas manifestaron que las prácticas responsables son importantes para ellas. Además, empresas que reportaron prácticas sostenibles, socialmente responsables o de gobernanza, crecieron 28%, mientras que aquellas que no lo hicieron crecieron 20%.

e) **Existen esfuerzos invaluables por brindar información y recomendaciones gratuitas a las empresas que no tienen la acogida ni el impacto deseable**. Este podría ser el caso la Modern Slavery Benchmarking Tool. En ese sentido, se hace necesario rescatar estos estos esfuerzos y divulgar su uso como una alternativa efectiva y de bajo coste para las empresas, y también confiable y transparente para los consumidores.

# 2. Objetivo
---
## 2.1. Objetivo General
Diseñar una herramienta de monitoreo y seguimiento que aliente y permita a las empresas evaluar e informar su progreso en la implementación de las recomendaciones para gestionar la esclavitud moderna proporcionadas por el Modern Slavery Benchmarking Tool de Walk Free.

## 2.1. Objetivos espécificos:

* Divulgar y facilitar la aplicación de la Modern Slavery Benchmarking Tool.
* Conectar a los consumidores con aquellas empresas que priorizan las acciones encaminadas a la garantía de los derechos humanos y la responsabilidad social.
* Conectar a proveedores y empresas cuyas prácticas de lucha contra la esclavitud moderna se alienen y generen sinergias de aprendizaje y retroalimentación. Consolidar repositorios de información relevante sobre la esclavitud moderna que permita sensibilizar a consumidores y empresas sobre la importancia de tomar acciones urgentes.
*  Garantizar el acceso a información que garantice trabajos y vidas dignas para las personas más vulnerables de ser víctimas de esclavitud moderna.
*  Diseñar un ChatBot que permita a los usuarios de la herramienta, tanto consumidores como empresas, acceder a información y funcionalidades de manera ágil y confiable.

# 3. Descripción Solución/Caso Uso de Datos
---
Respondiendo al planteamiento del problema y los objetivos trazados, nuestra propuesta de solución abarca dos enfoques. El primero involucra a las empresas en el reporte y transparencia con sus acciones específicas y el aprovechamiento de la Mondern Slavery Benchmarking Tool. Así, listamos a continuación las funcionalidades de LIBERTTRACK para las empresas:

* Reportar de manera voluntaria, autónoma y segura las acciones que se están implementando para luchar contra la esclavitud moderna y así mostrar a los consumidores, inversionistas, gobierno y ONG el trabajo y compromiso en la luchar contra la esclavitud moderna.
* Acceder a la *Modern Slavery Benchmarking Tool* para diligenciar el formulario de diagnóstico y tener en una lista de chequeo las acciones recomendadas para mejorar y mostrar los avances de la empresa.
* Que la información arrojada en la Modern Slavery Benchmarking Tool pueda ser (1) privada, (2) pública para los empleados o (3) pública para todas las personas según la estrategia de mejoramiento más conveniente.
* Registrar en la plataforma a los empleados y colaboradores para poder involucrarlos en las acciones de mejora emprendidas y sensibilizarlos sobre la esclavitud moderna.
* Acceder a información sobre qué es la esclavitud moderna y cuáles organizaciones trabajan sobre ella.
*  Acceder a una lista o catálogo de proveedores registrados cuyos principios empresariales se alineen con buenas prácticas, buenos puntajes y compromisos efectivos con la lucha contra la esclavitud moderna para favorecer alianzas o contratos de provisión de insumos.
*  Tener un asistente virtual ChatBot que pueda responder a mis preguntas sobre los puntos anteriores para facilitar mi navegación en la plataforma.

El segundo enfoque está relacionado con los consumidores y el rol primordial que juega la información para una adecuada respuesta de los mercados ante la esclavitud moderna. El diseño de nuestra herramienta LIBERTTRACK APP supone la facilidad de identificar con rapidez, tanto haciendo uso de la cámara para escanear los logotipos como de manera manual, las acciones que están llevando a cabo las empresas para luchar contra la esclavitud moderna. De igual manera LIBERTTRACK APP para consumidores contempla la implementación de acciones como:

* Saber la procedencia geográfica y las rutas que sigue la cadena de producción de la empresa que se consulta para identificar aquellas que involucran países o regiones en riesgo de esclavitud moderna.
* Saber si la empresa que se está consultando tiene información oficial o no. Es decir, si proviene de la misma empresa o está verificada en la plataforma empresarial.
* Tener detalles sobre las acciones que lleva a cabo la empresa para luchar contra la esclavitud moderna y así priorizar el consumo de aquellas que toman el tema con prioridad.
* Reportar o enviar alertas (con posibilidad de que sea anónima) sobre casos de esclavitud moderna vinculados con una empresa en particular para contribuir en la lucha contra la esclavitud moderna.
* Recibir sugerencias de empresas comprometidas con la lucha contra la esclavitud moderna
* Obtener información y recursos educativos sobre qué es la esclavitud moderna y cuáles son las organizaciones que trabajan en abolirla.
* Tener un asistente virtual ChatBot que pueda responder a mis preguntas sobre los puntos anteriores para facilitar mi navegación en la plataforma

**Sobre el prototipo LibertaTrack**

El diseño de nuestra herramienta cuenta con recursos explicativos anexos en el GitHub. Para su elaboración consideramos los Datasets entregados por los organizadores, así como la información pública de 5 restaurantes de cadena cuyos informes atienden a las exigencias de las leyes de Reino Unido. Por tanto, en la elaboración de esta propuesta fue esencial la información disponible en el Modern slavery statement registry de Reino Unido disponible en [Modern slavery statement registry - GOV.UK](modern-slavery-statement-registry.service.gov.uk).

# 4. Pitch
---
A continuacion el link del Pitch: 

[![LibertaTrack - DataJam Pasos Libres 2024](https://img.youtube.com/vi/ALWR6g8gBBA/0.jpg)](https://www.youtube.com/watch?v=ALWR6g8gBBA)


# 5. Datasets
---
Locación: /[datasets](modern-slavery-statement-registry.service.gov.uk)

* Base de conocimientos: [Knowledgebase](https://github.com/Datajam-Pasos-Libres-Online-2024/knowledgebase)

Los archivos listados son una serie de documentos en formato PDF que exploran el tema de la esclavitud moderna dentro de grandes cadenas de comida rápida y restaurantes. Cada archivo lleva el nombre de una cadena diferente, lo que indica que contienen información específica o reportes sobre las prácticas laborales de cada empresa respectivamente.


# 6. Código Proyecto
---
Locación: /[Organización de Github](https://github.com/orgs/Datajam-Pasos-Libres-Online-2024/repositories)

1. **Código del chatbot web**: [chatbot](https://github.com/Datajam-Pasos-Libres-Online-2024/chatbot-assistant)

* Frameworks: Streamlit.
* Servicios de AWS: AWS Lambda, Amazon CloudWatch, Amazon Bedrock, Amazon OpenSearch, Amazon API Gateway, Amazon CloudFormation.

3. **Base de conocimientos**: [Knowledgebase](https://github.com/Datajam-Pasos-Libres-Online-2024/knowledgebase)

* Frameworks: Ninguno.
* Servicios de AWS: Amazon S3.

5. **Aplicación web**: [liberta-track](https://github.com/Datajam-Pasos-Libres-Online-2024/liberta-track)

* Frameworks: Vue, TypeScript, React.
* Servicios de AWS: Amazon S3, Amazon Cognito, Amazon S3, Amazon Amplify.

7. **Aplicación móvil**: [libertaTrackApp](https://github.com/Datajam-Pasos-Libres-Online-2024/LibertaTrackApp)

* Frameworks: React Native.
* Servicios de AWS: Amazon S3: Amazon Cognito, Amazon S3, Amazon Amplify. 
  
9. **Infraestructura como código de AWS**: [liberta-track-cdk](https://github.com/Datajam-Pasos-Libres-Online-2024/liberta-track-cdk)

* Frameworks: React Native.
* Servicios de AWS: AWS Cloud Development Kit. 

Los repositorios listados corresponden a todo el código relacionado al desarrollo del chatbot, la aplicación web/móvil y el *deploy* de la arquitectura como código en AWS.

# 7. Documentos Adicionales (Opcional)
---
## 7.1. Demo de LibertaTrack y Tech Stack

A continuacion el link del demo de LibertaTrack y el Tech Stack:

[![LibertaTrack- Demo y Stack Tecnologico](https://img.youtube.com/vi/S7Z0mA_rRgI/0.jpg)](https://www.youtube.com/watch?v=S7Z0mA_rRgI)

## 7.2. Pasos para lanzar la infraestructura como código

Sigue estos pasos para desplegar con AWS CDK:

1. **Clona el Repositorio**: Ejecuta el siguiente comando para clonar este repositorio en tu máquina local:

```bash
git clone https://github.com/Datajam-Pasos-Libres-Online-2024/liberta-track-cdk.git
```

2. **Instalación**: Navega al directorio del proyecto e instala las dependencias utilizando npm o yarn.

```bash
cd your-repo-name
npm install   # or yarn install
```   

3. **Configuración**: Personaliza el proyecto según sea necesario editando archivos de configuración, como `.env`, y configurando tus puntos finales de API.

4. **Compilar el proyecto** (si tu proyecto utiliza TypeScript o algún otro lenguaje que necesite compilación):

```bash
cd your-repo-name
npm install   # or yarn install
```   

5. **Despliegue**:
- Ejecuta el comando de despliegue de CDK para desplegar tu stack en AWS:
  ```bash
  cdk deploy
  ```
- Si tienes múltiples stacks o necesitas especificar configuraciones adicionales, puedes agregar los nombres de los stacks y opciones adicionales:
  ```bash
  cdk deploy nombre-del-stack --parameters miParametro=valor
  ```
6. **Verificación**: Verifica que los recursos se hayan desplegado correctamente en la consola de AWS o utilizando el AWS CLI para listar los recursos.

Recuerda que el AWS CDK te permite definir tu infraestructura en código y desplegarla mediante comandos. Asegúrate de tener la última versión del CDK instalada para evitar problemas de compatibilidad con las nuevas características de AWS.

## 7.3. Instrucciones para ejecutar la aplicación móvil de forma local

Sigue estos pasos para comenzar con la aplicacón móvil:

1. **Clona el Repositorio**: Ejecuta el siguiente comando para clonar este repositorio en tu máquina local:

```bash
git clone https://github.com/Datajam-Pasos-Libres-Online-2024/LibertaTrackApp.git
```

2. **Instalación**: Navega al directorio del proyecto e instala las dependencias utilizando npm o yarn.

```bash
cd your-repo-name
npm install   # or yarn install
```   

3. **Configuración**: Personaliza el proyecto según sea necesario editando archivos de configuración, como `.env`, y configurando tus puntos finales de API.

4. **Ejecución en desarrollo**:
- Para iOS:
  ```bash
  npx react-native run-ios
  ```
- Para Android:
  ```bash
  npx react-native run-android
  ``` 

5. **Construcción para producción**:
- Para iOS, utiliza Xcode para construir tu aplicación para producción.
- Para Android, sigue estos pasos para generar un APK o un AAB:
  ```
  cd android
  ./gradlew bundleRelease  # Para AAB
  ./gradlew assembleRelease  # Para APK
  ```

Recuerda que debes tener configurado el ambiente de desarrollo para React Native, incluyendo Node.js, Watchman, el Android SDK, y Xcode si estás desarrollando para iOS.

![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/58c96f6e-1994-4ed5-9541-e0da84ac8f93)
![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/048db797-a51d-4d69-b1a0-e94c22e91249)
![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/e796cb58-63e1-4b64-8108-5122b57b1649)

## 7.4. Instrucciones para ejecutar la aplicación web de forma local

Sigue estos pasos para empezar con la aplicación web:

1. **Clona el Repositorio**: Ejecuta el siguiente comando para clonar este repositorio en tu máquina local:

```bash
git clone https://github.com/Datajam-Pasos-Libres-Online-2024/liberta-track.git
```

2. **Instalación**: Navega al directorio del proyecto e instala las dependencias utilizando tu gestor de paquetes preferido:

```bash
cd your-repo-name
npm install   # or yarn install
```   

3. **Configuración**: Personaliza el proyecto según sea necesario editando archivos de configuración, como `.env`, y configurando tus puntos finales de API.

4. **Desarrollo**: Inicia el servidor de desarrollo:

```bash
npm run dev   # or yarn dev
```   

5. **Construcción para Producción**: Cuando tu proyecto esté listo para el despliegue, crea una construcción de producción:

```bash
npm run build   # or yarn build
```

![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/20546ffe-cbea-475f-bc68-2a10b9d623a6)
![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/0c1186ce-6020-4638-8d7f-311953fed9d4)
![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/5b41047e-7880-4f8a-9f98-26f5cf6c1d6a)
![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/96358f66-502c-4234-be1a-59c7260122bd)
![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/7eea30b6-ea9b-4934-a420-e22bc19bba90)
![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/ab64fa56-9792-4916-9b97-80844b1cad4d)
![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/e19bccf0-7ec9-41fa-b7a6-ddea1a5d651f)
![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/90d37ef5-3f64-47bf-a1e9-194094fe3aea)
![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/01362d7f-21a1-43f3-90d8-6fb7fdd85e48)
![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/865bd9b9-9275-46e3-ac33-51f079e2fb09)


## 7.5. Arquitectura de solución del chatbot en AWS

A continuación se presenta la arquitectura de solución realizada del chabot en AWS:

![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/e33c9cad-23c6-47a4-bd64-9cb6918fb606)

La arquitectura mostrado es para un chatbot que opera utilizando diversos servicios de AWS (Amazon Web Services). Aquí se detalla cómo funciona cada componente de esta arquitectura:

1. **Cliente**: Representa al usuario final que interactúa con el chatbot. Este puede ser cualquier dispositivo o interfaz que envía preguntas al chatbot.

2. **LLM Response (Respuesta de Modelo de Lenguaje Grande)**: Este componente es el encargado de procesar la entrada del usuario (la pregunta) y generar una respuesta utilizando el modelo de Claude 2.1.

3. **AWS Lambda**: Es un servicio de computación sin servidor que ejecuta código en respuesta a eventos. En esta arquitectura, Lambda manejan la lógica de negocio del chatbot, como recibir preguntas del cliente, enviarlas al modelo de lenguaje, recibir la respuesta y luego devolverla al cliente.

4. **Amazon Bedrock**: Amazon Bedrock es un servicio totalmente administrado que ofrece una selección de modelos fundacionales (FM) de alto rendimiento de las principales empresas de IA como AI21 Labs, Anthropic, Cohere, Meta, Mistral AI, Stability AI y Amazon a través de una sola API. Para este caso, se personalizo de forma privada con los datos  de las empresas mediante la téncnica de generación aumentada de recuperación (RAG).

5. **Amazon OpenSearch Service**: Este servicio permite la búsqueda y análisis de grandes volúmenes de datos. En el contexto de un chatbot, se usa como base de datos vectorial para buscar respuestas o información relevante en un conjunto de datos, basándose en la entrada del usuario.

6. **Amazon Simple Storage Service (Amazon S3)**: Este es un servicio de almacenamiento de objetos que ofrece escala, disponibilidad de datos, seguridad y rendimiento. Aquí, se utiliza para almacenar los documentos de las empresas que el chatbot podría necesitar consultar.

7. **AWS CloudFormation**: Permite a los desarrolladores y a las empresas automatizar el despliegue y la gestión de la infraestructura como código. En esta arquitectura, se utiliza para orquestar y manejar la creación y gestión de todos los recursos AWS utilizados por el chatbot.

## 7.6. Propuesta de la arquitectura de solución en etapa de producción

A continuación se presenta la arquitectura de solución propuesta si se optará por sacar la aplicación web a producción:

![image](https://github.com/DataJam-Pasos-Libres-2024/LibertaTrack/assets/69759418/b2359630-ccee-459a-b26a-d096958e6f6b) 

La arquitectura presentada en el diagrama garantiza una aplicación con un enfoque en alta disponibilidad, escalabilidad y seguridad. Aquí se detallan estos aspectos:

1. **Alta Disponibilidad**:

* **Zona de disponibilidad**: La infraestructura se despliega en múltiples zonas de disponibilidad (AZs). En este caso, AZ A y AZ B. Esto asegura que si una zona tiene una falla, la otra puede continuar operando, minimizando el tiempo de inactividad.

* **Balanceadores de carga**: Se utilizan dos tipos de balanceadores de carga: uno externo (Internet Load Balancer) para distribuir el tráfico entrante desde Internet, y otro interno (Internal Load Balancer) para distribuir el tráfico entre los servidores web y otros componentes internos. Esto no solo distribuye eficientemente el tráfico, sino que también proporciona tolerancia a fallos si un servidor se cae.

2. **Escalabilidad**:

* **Auto Scaling Groups**: Hay dos grupos de autoescalado en la arquitectura, uno para el frontend y otro para el backend. Estos grupos ajustan automáticamente el número de instancias EC2 (t2.medium en este caso) según la demanda para mantener el rendimiento y minimizar costos.

* **Subredes públicas y privadas**: Utilizar subredes diferenciadas para diferentes propósitos (públicas para exposición a internet y privadas para procesos internos) permite una gestión más eficiente de los recursos y facilita la escalabilidad vertical y horizontal según sea necesario.

3. **Seguridad**

* **Subredes privadas y públicas**: Los componentes críticos como bases de datos MySQL y servidores web están ubicados en subredes privadas, lo que limita el acceso directo desde Internet, aumentando la seguridad.
  
* **NAT Gateways**: Ubicados en subredes públicas, los NAT Gateways permiten que las instancias en las subredes privadas accedan a Internet para actualizaciones y parches, sin permitir conexiones entrantes desde Internet, protegiendo así estas instancias.

* **Internet Gateway y Endpoint de gateway**:  El Internet Gateway permite la comunicación entre los recursos de AWS en la VPC y el Internet, mientras que el Endpoint de gateway se utiliza para conexiones seguras a servicios de AWS, como el bucket de S3, sin necesidad de exponer el tráfico a Internet público.

4. **Otros aspectos**:

* **S3 Bucket**: Utilizado para almacenar datos estáticos o backups, que pueden ser accedidos de manera segura a través del Gateway Endpoint.

* **MySQL Instances**: La base de datos principal y una instancia alternativa proporcionan redundancia y aseguran la persistencia de datos entre las zonas de disponibilidad.

Esta arquitectura proporciona una solución robusta para LibertaTrack web que requieren un alto nivel de operatividad, adaptabilidad ante cambios de carga y una defensa sólida contra accesos no autorizados y otros riesgos de seguridad por datos sensibles de las empresas.

# 8. Referencias
---
* Alvarado, F., Álvarez, A., Chaparro, J. C., González, C., Levy, S., Maldonado, D., ... & Villaveces, M. J. (2021). Reporte ejecutivo de la Misión de Empleo de Colombia. Bogotá, DC, Colombia: Ministerio de Trabajo-DNP.
* AU Modern Slavery Act 2018. An Act to require some entities to report on the risks of modern slavery in their operations and supply chains and actions to address those risks, and for related purposes. 10th December 2018.
* CA S.C. 2023, c. 9. An Act to enact the Fighting Against Forced Labour and Child Labour in Supply Chains Act and to amend the Customs Tariff. 1th May 2023
* Frey, S. B. A. J., Am, J. B., Doshi, V., Malik, A., & Noble, S. (2023). Consumers Care about Sustainability and Back It Up with Their Wallets. Mckinsey and Company
* UK Modern Slavery Act 2015. An Act to make provision about slavery, servitude and forced or compulsory labour and about human trafficking, including provision for the protection of victims; to make provision for an Independent Anti-slavery Commissioner; and for connected purposes. 26th March 2015. 
* Walk Free (2023). The Global Slavery Index 2023, Minderoo Foundation. Recuperado de https://walkfree.org/global-slavery-index
