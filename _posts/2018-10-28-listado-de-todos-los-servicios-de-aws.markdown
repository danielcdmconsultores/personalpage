---
title: Listado de todos los Servicios de AWS
date: 2018-10-28 11:16:00 +01:00
---

Siempre he querido tener un listado de TODOS los servicios de AWS y una breve descripción (párrafo) + vídeo descriptivo, a modo de recuerdo o "chuleta". Por favor si lo encuentras de utilidad, haz mención y entre tod@s vamos ampliando este listado.

En solo 30 minutos entenderás todos los servicios que ofrece la nube pública más popular, AWS.
Computación (máquina)
EC2: Genera máquinas virtuales elásticas y escalables. De computo general, hasta 12 Tera Bytes RAM, o complejas con GPUs, alto rendimiento... [VIDEO]
Lightsail: Las máquinas virtuales básicas (Linux y Windows), para competir en precio, con menos prestaciones, no convertibles en EC2 (de momento). Ahora también MySQL multi-az para desacoplar la aplicación.[VIDEO]
Lambda: Las funciones en serverless (sin servidor), pago por uso en llamadas a las funciones (Node.js, Python, Java, C# y Go.).[VIDEO]
Batch: Procesamiento por lotes totalmente administrado para cualquier escala.[VIDEO]
Elastic Beanstalk: Para implementar y escalar servicios y aplicaciones web desarrollados con Java, NET, PHP, Node.js, Python, Ruby, Go y Docker en servidores familiares como Apache, Nginx, Passenger e IIS. (genera EC2).[VIDEO]
Amazon EKS: Amazon Elastic Container Service for Kubernetes es un servicio administrado que le permite ejecutar fácilmente Kubernetes en AWS sin necesidad de instalar ni usar sus propios clústeres de Kubernetes. [VIDEO]
Fargate: Te permite ejecutar contenedores sin tener que administrar servidores ni clústeres. Ya no tendrá que aprovisionar, configurar ni escalar clústeres de máquinas virtuales para ejecutar los contenedores[VIDEO]
Elastic Container Service: Servicio de administrador de contenedores compatible con Dockers. [VIDEO]
 Almacenamiento
S3: Almacenamiento de objetos con 99.999999999% durability (para guardar ficheros, backups, imágenes, etc) (no confundir con un dropbox, aunque tiene similitudes). [VIDEO]
EBS: Almacenamiento a nivel de bloque de Sistema Operativo. [VIDEO]
EFS: Almacenamiento en red para instancias EC2, como un NAS-iscsi. [VIDEO]
Glacier: Para backups a largo plazo, duradero y a bajo coste. [VIDEO]
Storage Gateway: Conector de tu NAS on-premise al S3.[VIDEO]
Snowball: Solución de transporte de datos (Hardware) a escala de petabytes que utiliza dispositivos diseñados para ser seguros y para transferir grandes volúmenes de datos hacia y desde la nube de AWS [VIDEO]
Snowmobile: Snowball pero a lo bestia (a escala de exabytes), hasta 100 PB en un contenedor para transportarlo en un camión. [VIDEO]
 Bases de datos
RDS: Las Bases de datos relacionales administradas, MsSQL, MySQL, MariaDB, PostgresSQL y escalable, etc...[VIDEO]
Aurora: Base de datos Relacional, compatible MySQL, PostgresSQL. Aurora es hasta cinco veces más rápida que las bases de datos de MySQL estándar y tres veces más rápida que las bases de datos de PostgreSQL estándar. [VIDEO]
DynamoDB: Base de datos no relacional (no-sql), super-rápida y auto-escalable, con un 99.999 % SLA [VIDEO]
ElastiCache: Caches o datastores en memoria. Compatible con Redis y Memcached.[VIDEO]
Amazon Redshift: Para almacenamiento de datos para BI (permite ejecutar consultas complejas en petabytes).[VIDEO]
Neptune: Servicio de base de datos de gráficos rápido, de confianza y totalmente administrado que le permite crear y ejecutar fácilmente aplicaciones que funcionen con conjuntos de datos muy conectados [VIDEO]
 Red y contenido
VPC: Red Aislada dentro de tu entorno en la nube. [VIDEO]
CloudFront: El CDN de amazon (con 106 ubicaciones de borde). [VIDEO]
Direct Connect: Conexión de red dedicada con amazon a su red/ubicación on-premise. [VIDEO]
Route 53: Un potente gestor DNS. [VIDEO]
API Gateway: Facilita a los desarrolladores la creación, la publicación, el mantenimiento, la monitorización y la protección de API a cualquier escala [VIDEO]
AWS PrivateLink: Permite conectar VPC directamente sin pasar por Internet y válido para que on-premise use servicios de AWS de forma privada [VIDEO]
 Migración
AWS Migration Hub: Ofrece una ubicación única para realizar el seguimiento de los avances de las migraciones de aplicaciones en varias soluciones de AWS y otras empresas del sector. [VIDEO]
Application Discovery Service: Ayuda a los clientes empresariales a planificar proyectos de migración al recopilar información sobre sus centros de datos on-premise. [VIDEO]
Database Migration Service: Ayuda a migrar las bases de datos a AWS de manera rápida y segura. [VIDEO]
Server Migration Service: Servicio sin agente que le permite migrar de forma más rápida y sencilla miles de cargas de trabajo on-premise a AWS. Con AWS SMS, puede automatizar, programar y monitorizar replicaciones incrementales de volúmenes de servidores en vivo, lo que facilita la coordinación de migraciones de servidores a gran escala. [VIDEO]
 Herramientas de desarrollo
CodeStar: Facilita la configuración de toda la cadena de herramientas de desarrollo y entrega continua para codificar, compilar, probar e implementar el código de la aplicación. Para comenzar un proyecto, puede elegir entre varias plantillas de Amazon EC2, AWS Lambda y AWS Elastic Beanstalk. [VIDEO]
CodeCommit: Servicio de control de código fuente totalmente administrado que facilita a las empresas el hospedaje de repositorios Git privados, seguros y altamente escalables. [VIDEO]
CodeBuild: Es un servicio de creación totalmente administrado que crea código fuente, ejecuta pruebas y produce paquetes de software listos para su implementación. No es necesario aprovisionar, administrar y escalar sus propios servidores de creación.[VIDEO]
CodeDeploy: Servicio que automatiza las implementaciones de código en cualquier instancia, incluidas las instancias de Amazon EC2 y aquellas ejecutadas on-premise.[VIDEO]
CodePipeline: Es un servicio de integración continua y entrega continua para realizar actualizaciones de aplicaciones e infraestructura rápidas y de confianza. CodePipeline compila, prueba e implementa el código cada vez que se produce un cambio en este, de acuerdo con los modelos de procesamiento de la publicación que defina. [VIDEO]
X-Ray: Ayuda a desarrolladores a analizar y depurar aplicaciones distribuidas de producción, como las creadas con una arquitectura de micro-servicios [VIDEO]
Cloud9: Un IDE en la nube, permite escribir código, ejecutar y depurar solamente con un navegador, incluye un terminal con las CLI todo pre-configurado. [VIDEO]
SDK: Completo set de juegos que ayuda a que su aplicación obtenga acceso directo a los servicios de Amazon, incluidos AWS Lambda, S3, DynamoDB, entre otros. Los SDK para dispositivos móviles son compatibles con iOS, Android, Web, React Native, Unity y Xamarin. [VIDEO]
Amplify: Una librería Java Script para desarrolladores de aplicaciones para usar los Servicios Cloud [VIDEO]
Herramientas de Administración
CloudWatch: Monitoriza los servicios de AWS con métricas, disparadores, etc... [VIDEO]
CLI: Interface de línea de comandos para Mac, linux, Windows, para poder controlar varios servicios de AWS desde la línea de comando y automatizarlos mediante secuencias de comandos. [VIDEO]
CloudFormation: Creador de mundos de AWS todo con scripts (yaml y json). [VIDEO]
CloudTrail: Permite realizar regulaciones y auditorías operativas, de riesgo/seguridad y conformidad en su cuenta de AWS. [VIDEO]
Config: Permite examinar, auditar y evaluar las configuraciones de sus recursos de AWS. [VIDEO]
OpsWorks: Administración de configuraciones que utiliza Chef, una plataforma de automatización que trata las configuraciones de servidor como código. [VIDEO]
Service Catalog: Permite a las organizaciones crear y administrar catálogos de servicios de TI aprobados para su uso en AWS. Incluye todo lo relacionado con imágenes, servidores, software y bases de datos de máquinas virtuales para completar las arquitecturas de aplicaciones multi-nivel. [VIDEO]
Trusted Advisor: Ayuda a reducir los costos, incrementar el desempeño y mejorar la seguridad al optimizar el entorno de AWS, proporciona asesoramiento a tiempo real para ayudarle a aprovisionar los recursos de acuerdo con las prácticas recomendadas de AWS. [VIDEO]
Systems Manager: Recabe información operativa e implemente acciones en recursos: Unifica, agrupa y automatiza tareas operativas de los recursos. Permite conectarse a las instancias (Windows/Linux) sin abrir puertos ni claves .PEM (Session Manager) [VIDEO]
Personal Health Dashboard proporciona alertas y orientación para solucionar problemas en caso de que AWS esté experimentando eventos que puedan afectarle [VIDEO]
Servicios Multi-media
Elastic Transcoder: Realiza tareas de trans-codificación de contenido. [VIDEO]
Kinesis Video Streams: Aprendizaje automático y tareas analíticas [VIDEO]
Elemental MediaConvert: Trans-codificador de vídeos basado en archivos con características de emisión. [VIDEO]
Elemental MediaLive: Procesamiento de vídeo en directo para emisión [VIDEO]
Elemental MediaPackage: Prepare y proteja fácilmente vídeos para entrega bajo demanda y en directo. [VIDEO]
Elemental MediaStore: Ofrece nivel de desempeño, consistencia y baja latencia para entrega de vídeo. [VIDEO]
Elemental MediaTailor: Inserta anuncios focalizados individualmente en sus transmisiones de vídeo. [VIDEO]
Identidad, Seguridad y Conformidad.
IAM: Controle el acceso de forma segura a los servicios y recursos de AWS de sus usuarios. [VIDEO]
Inspector: Servicio de evaluación de seguridad automatizado para ayudar a mejorar la seguridad y la conformidad de las aplicaciones implementadas en AWS. [VIDEO]
Certificate Manager: Permite aprovisionar, administrar e implementar con facilidad certificados de capa de conexión segura/seguridad de la capa de transporte (SSL/TLS) para su uso con servicios de AWS. [VIDEO]
Directory Service: Microsoft AD - Active Directory administrado en la nube de AWS. Migre con facilidad aplicaciones y cargas de trabajo compatibles con el directorio, disponible también como (Standard Edition)[VIDEO]
WAF & Shield: Un cortafuegos de aplicación web que permite monitorizar accesos a tu CloudFront o evitar DDoS.[VIDEO]
Artifact: Portal de auditoría y conformidad para el acceso bajo demanda, permite descargar los informes de conformidad (pdf) de AWS y administrar acuerdos seleccionados.[VIDEO]
Amazon Macie: Es un servicio de seguridad que utiliza el aprendizaje automático para descubrir, clasificar y proteger datos confidenciales automáticamente en AWS. Reconoce los datos confidenciales, como la información personalmente identificable (PII) o la propiedad intelectual y le proporciona paneles de control y alertas que aportan visibilidad acerca de cómo se están trasladando estos datos o se está accediendo a ellos.[VIDEO]
CloudHSM: Es un módulo de seguridad de hardware (HSM) basado en la nube que le permite generar con facilidad y usar sus propias claves de cifrado en la nube de AWS. [VIDEO]
GuardDuty: Es un servicio de detección de amenazas administradas que monitorea continuamente el comportamiento malicioso o no autorizado para proteger sus cuentas y cargas de trabajo de AWS. Supervisa la actividad, como llamadas API inusuales o implementaciones potencialmente no autorizadas que indican un posible compromiso de la cuenta. GuardDuty también detecta instancias potencialmente comprometidas. [VIDEO]
Cognito: Permite agregar el registro y el inicio de sesión de forma sencilla a sus aplicaciones web y móviles. También tiene las opciones de autenticar a los usuarios a través de proveedores de identidad social, como Facebook, Twitter o Amazon, con soluciones de identidad SAML. [VIDEO]
Single Sign-on: Administre de maneda centralizada el acceso con inicio de sesion único a varias aplicaciones empresariales de AWS. [VIDEO]
 Analítica
Athena: Es un servicio de consultas interactivo que facilita el análisis de datos en Amazon S3 con SQL estándar. Athena no tiene servidor, de manera que no es necesario administrar infraestructura y solo paga por las consultas que ejecuta.[VIDEO]
EMR: Proporciona un marco Hadoop hospedado que facilita, acelera y rentabiliza procesar enormes cantidades de datos en instancias Amazon EC2 dinámicamente escalables. [VIDEO]
CloudSearch: servicio administrado en la nube de AWS que facilita la configuración, la administración y el escalado rentables de una solución de búsqueda para su sitio web o aplicación. [VIDEO]
Elasticsearch Service: Facilita la implementación, el uso y el escalado de Elasticsearch para el análisis de logs, la búsqueda de texto completo, la monitorización de aplicaciones y mucho más.[VIDEO]
Kinesis: Facilita la recopilación, el procesamiento y el análisis de datos de streaming en tiempo real para obtener conocimiento de manera oportuna y reaccionar rápidamente ante información nueva. [VIDEO]
Data Pipeline: Servicio web pensado para ayudarle a procesar datos y a transferirlos, de manera fiable y a intervalos definidos, entre diferentes servicios de almacenamiento e informática de AWS, así como entre orígenes de datos on-premise. [VIDEO]
QuickSight: El rápido y fácil BI (Business Intelligence) de amazon, a una décima parte del precio. [VIDEO]
AWS Glue: Servicio de extracción, transformación y carga (ETL) totalmente administrado que facilita a los clientes la preparación y carga de sus datos para su análisis. [VIDEO]
 Inteligencia Artificial - Machine Learning
Lex: Servicio para crear interfaces de conversación en cualquier aplicación con voz y texto. [VIDEO]
Amazon Polly: Convierte texto en habla realista, lo que permite crear aplicaciones y categorías totalmente nuevas de productos con esta capacidad. [VIDEO]
Rekognition: Facilita la agregación de análisis de imágenes a sus aplicaciones. Puede detectar objetos, escenas, rostros; reconocer a famosos; e identificar contenido inapropiado en las imágenes. [VIDEO]
Tensorflow: Se ha convertido en una opción popular para la investigación de aprendizaje profundo y desarrollo de aplicaciones, en particular en áreas como la visión por computadora, la comprensión del lenguaje natural y la traducción del habla. [VIDEO]
Machine Learning: Facilita a desarrolladores de todos los niveles de habilidad el uso de la tecnología de aprendizaje automático. Amazon Machine Learning proporciona asistentes y herramientas de visualización que le guían a lo largo del proceso de creación de modelos de aprendizaje automático (ML) sin tener que aprender complicados algoritmos y tecnología de ML [VIDEO]
Amazon Translate: Permite traducir grandes volúmenes grandes de texto de manera sencilla y eficiente, así como localizar sitios web y aplicaciones para los usuarios internacionales. [VIDEO]
Amazon Transcribe: Reconocimiento de voz automático (ASR) y por supuesto con API [VIDEO].
SageMaker : Cree, entrene e implemente modelos de aprendizaje automático a escala [VIDEO]
DeepLens: La primera cámara de vídeo (Hardware) con aprendizaje profundo para programadores. Si quieres verla funcionando en Bilbao, llámame. [VIDEO]
Amazon Comprehend: Servicio de procesamiento de lenguaje natural (NLP) que usa el aprendizaje automático para encontrar información y relaciones en el texto [VIDEO]
Apache MXNet es un marco rápido de inferencia y entrenamiento de escala ajustable con un API concisa y fácil de usar para aprendizaje automático. [VIDEO]
 Internet de las cosas (IoT)
IoT Core: Gestión de Internet de las Cosas y conexión con el ecosistema de AWS. [VIDEO]
IoT 1 click: Permite a dispositivos sencillos activar funciones de AWS Lambda que pueden ejecutar una acción [VIDEO]
IoT Device Management: Incorpore, organice, monitorice y administre de manera remota dispositivos conectados a escala [VIDEO]
IoT Device Defender: Servicio completamente administrado que lo ayuda a asegurar su flota de dispositivos de IoT. [VIDEO]
FreeRTOS: Sistema Operativo con funciones IoT para micro-controladores [VIDEO]
AWS Greengrass: Es software que le permite ejecutar capacidades de informática local, mensajería, almacenamiento de datos en caché y sincronización para dispositivos conectados de manera segura para IoT. [VIDEO]
 Centro de contacto / Atención al cliente
Amazon Connect: Servicio de centro de contacto (centralita) basado en la nube con modalidad autoservicio que le permite a cualquier empresa ofrecer un mejor servicio al cliente con facilidad y a un costo menor. [VIDEO]
Simple Email Service: Plataforma de envío y recepción de emails super-escalable.[VIDEO]
Pinpoint Facilita el envío de mensajes a usuarios directamente desde su aplicación o servicio de backend, así como ejecutar campañas focalizadas para mejorar la interacción de los usuarios.[VIDEO]
 Desarrollo de juegos
Amazon GameLift: Servicio administrado para implementar, utilizar y escalar servidores de videojuegos dedicados para videojuegos multi-jugador basados en sesiones. [VIDEO]
Amazon Lumberyard: Es un motor de videojuegos AAA gratuito con un profundo nivel de integración con AWS y Twitch. Puedes dercargar gratis la aplicación para Windows [VIDEO]
Amazon GameOn: Es un set deAPI para desarrolladores de juegos que permite tener a tus jugadores más entretenidos o conectado con el comercio electrónico de amazon para que los jugadores ganen premios. [VIDEO]
 Servicios móviles
Mobile Hub: Simplifica el proceso de construir, probar y monitorizar aplicaciones móviles que usan servicios de AWS. [VIDEO]
Device Farm: Mejore la calidad de las aplicaciones iOS, Android y web probándolas en dispositivos móviles reales en la nube de AWS. [VIDEO]
Mobile Analytics: Recopile, visualice y exporte análisis de la aplicación. [VIDEO]
AppSync: Crea aplicaciones guiadas por datos con capacidades en tiempo real y sin conexión. [VIDEO]
AR / VR Realidad Aumentada / Realidad Virtual
Sumerian: Crear experiencias tridimensionales, de VR y AR. [VIDEO]
Integración de aplicaciones
Step Functions: Cree aplicaciones distribuidas con flujos de trabajo visuales. [VIDEO]
MQ: Servicio de agente de mensajes administrado para Apache ActiveMQ [VIDEO]
Simple Queue Service: Colas de mensajes completamente administradas para micro-servicios, sistemas distribuidos y aplicaciones sin servidor. [VIDEO]
Simple Notification Service: Notificaciones móviles y mensajes de publicación/suscripción para micro-servicios, sistemas distribuidos y aplicaciones sin servidor. [VIDEO]
SWF: Ayuda a los desarrolladores a diseñar, ejecutar y escalar trabajos de fondo que siguen pasos paralelos o secuenciales. [VIDEO]
 Productividad Empresarial
Alexa para negocios: El "SIRI" de Amazon se llama Alexa y ahora está especializado para ayuda en el trabajo: [VIDEO]
WorkDocs: Servicio empresarial seguro de almacenamiento y uso compartido totalmente administrado con controles administrativos estrictos y funciones de comentarios que mejoran la productividad de los usuarios, tipo dropbox. [VIDEO]
WorkMail: Servicio de email y calendario empresarial tipo webmail, seguro y administrado que soporta las aplicaciones clientes de email para dispositivos móviles y de escritorio existentes. pop3 y smtp. [VIDEO]
Amazon Chime: VideoConferencia de amazon, alternativa a Skype. [VIDEO]
 Escritorio y transmisión de aplicaciones
WorkSpaces: Solución de escritorio virtual (Windows 7, Windows 10 o Amazon Linux 2) como servicio (DaaS) segura y completamente administrada que se ejecuta en AWS. [VIDEO]
AppStream 2.0: Permite enviar las aplicaciones de Windows a cualquier dispositivo. [VIDEO]


NOTA: Recuerda compartir esta publicación, si ves algún servicio mal explicado o nuevo que no esté en este documento, házmelo saber...

Links de interés:
Presentación en Español de Novedades AWS 2017

AWS Summit MADRID 2018﻿

AWS DataBase Blog

Grupo de usuarios en Bilbao bilbaws.com

