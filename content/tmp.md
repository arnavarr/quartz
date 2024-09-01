- Identificador: MC-EPS.05

- Capa de Seguridad: Managed Clients

- Principio: Establecer controles con objeto de proteger los dispositivos gestionados frente a amenazas cibernéticas.

- Objetivo: Establecer los controles que permitan hacer cumplir las políticas de seguridad sobre dispositivos móviles (end points) corporativos o de entorno BYOD -- MDM, así como hacer cumplir las políticas de seguridad a nivel de aplicación, tales como browsers, clientes de correo, aplicaciones desarrolladas para la empresa, etc. - MAM.

- Consideraciones al control:
    - Haga uso de soluciones MDM con objeto de hacer cumplir las políticas de seguridad sobre los dispositivos gestionados de ámbito corporativo o BYOD.
    - Haga uso de un catálogo de aplicaciones permitidas y establezca políticas a nivel granular mediante el uso de soluciones de tipo MAM.
    - Garantice un control total sobre los endpoints de forma centralizada haciendo cumplir políticas tales como autenticación y autorización de usuarios, gestión de aplicaciones permitidas, políticas de eliminación de datos frente a robos, bastionado, etc.


---


- Identificador: MC-EPS.06

- Capa de Seguridad: Managed Clients

- Principio: Establecer controles con objeto de proteger los dispositivos gestionados frente a amenazas cibernéticas.

- Objetivo: Hacer uso de los sistemas o procedimientos ágiles, que garanticen la implementación de las Best Security Guides y/o Hardening Guides de los distintos fabricantes de software y hardware con objeto de reducir la superficie de ataque sobre los dispositivos gestionados por la compañía.

- Consideraciones al control:
    - Siempre que sea posible, haga uso de sistemas que permitan agilizar la implantación de las guías de mejores prácticas de seguridad y/o guías de bastionado sobre los dispositivos gestionados por la compañía.
    - Establezca los procedimientos que permitan garantizar el ciclo de vida de implantación de dichas guías.
    - Implemente el bastionado a nivel de hardware y software y de aplicaciones.


---



- Identificador: MC-EPS.07

- Capa de Seguridad: Managed Clients

- Principio: Establecer controles con objeto de proteger los dispositivos gestionados frente a amenazas cibernéticas.

- Objetivo: Como parte de la primera línea de defensa, establecer mecanismos que proporcionen defensa contra amenazas cibernéticas tales como software malicioso, threats.

1. Certified Device

- Identificador: MC-EPS.08

- Capa de Seguridad: Managed Clients

- Principio: Establecer controles con objeto de proteger los dispositivos gestionados frente a amenazas cibernéticas.

- Objetivo: Garantizar que los dispositivos y su software cumplen con los requerimientos específicos en criterios de seguridad.

- Consideraciones al control:
    - Deberá garantizar que los dispositivos gestionados y el software del cual hace uso, ya bien sean de ámbito corporativo o de ámbito BYOD, cumplen con los requerimientos específicos en materia de ciberseguridad. Para ello, deberá garantizar el cumplimiento del resto de controles.


----


- Identificador: I-BS.01

- Capa de Seguridad: Boundary Security

- Principio: Establecer controles con objeto de proteger la infraestructura y sus activos frente a amenazas cibernéticas del exterior.

- Objetivo: Establecer mecanismos que permitan filtrar y proteger los servicios de la infraestructura expuestos hacia redes no confiables.

- Consideraciones al control:
    - Hacer uso de una arquitectura de seguridad de redes en capas que garantice el control de flujos Norte-Sur y Sur-Norte para todos los casos.
    - Hacer uso de soluciones que permitan dar gobernanza centralizada de las políticas de control de red sobre los flujos anteriormente citados.
    - Cerciórese que dada una solución, esta cuenta con mecanismos avanzados de protección tales como stateful inspection, packet filtering, zone-based segmentation, policy-based, bi-direccional SSL/TLS Decryption, TCP Protocol Validation, threat prevention, URL filtering o Navigation filtering, File and Data Filtering, entre otros, que permitan cubrir total o parcialmente los criterios de ciberseguridad en la arquitectura derivados de los restantes controles necesarios y listados en este Marco.
    - Deberá hacer uso de reglas específicas y siempre que sea posible hacer uso de políticas con base en:
        - Políticas basadas en IP, puerto y protocolo.
        - Políticas basadas en aplicaciones.
        - Políticas basadas en identificación de usuarios.
        - Políticas basadas en actividad de red.


---


- Identificador: I-BS.02

- Capa de Seguridad: Boundary Security

- Principio: Establecer controles con objeto de proteger la infraestructura y sus activos frente a amenazas cibernéticas del exterior.

- Objetivo: Emplear sistemas de detección y prevención de intrusos que inspeccionen la red y el contenido del tráfico, integrados con el sistema de gestión de incidentes y eventos de seguridad.

- Consideraciones al control:
    - Confirme que los sistemas de detección de intrusiones y prevención de intrusiones de red (IDS/IPS) están activos y configurados para inspeccionar al menos el tráfico Norte-Sur y tránsitos Este-Oeste que provengan de ubicaciones externas no confiables, hacia DMZ o hacia redes internas con servicios "sensibles".
    - Asegúrese que la funcionalidad queda implementada para todo tipo de puerto y protocolo. Además, tenga en cuenta que deberá implementar dicha funcionalidad junto con TLS Decryption para aquel tráfico encriptado cuya naturaleza origen no atraviese las soluciones de WAF.
    - Además, asegúrese de que IDS/IPS siempre esté optimizado para proporcionar alertas de alta calidad a la solución SIEM desplegada.


---

- Identificador: I-BS.03

- Capa de Seguridad: Boundary Security

- Principio: Establecer controles con objeto de proteger la infraestructura y sus activos frente a amenazas cibernéticas del exterior.

- Objetivo: Establecer aislamiento lógico entre redes de diferente confiabilidad con objeto de proporcionar mayor segmentación lógica, granularidad en la operación/orquestación de las políticas de seguridad y monitorización.

- Consideraciones al control:
    - Asegúrese que implementa una zona desmilitarizada (DMZ) en un segmento lógico separado, de forma que proporcione una capa adicional de seguridad entre los activos y las redes no confiables.
    - Utilice la red desmilitarizada para el control de acceso, supervisión, registro, activación de mecanismos de prevención de denegación de servicio, sistemas de detección/prevención de intrusiones, reglas y políticas en los cortafuegos, filtrado web, antimalware, entre otros.
    - Evite utilizar una topología Mesh (en malla) implementando en su lugar una arquitectura basada en estrella, permitiendo así aislar las cargas de trabajo, facilitando la implementación de una red desmilitarizada e introduciendo identidad y seguridad a la solución.
    - Certifique que el punto central de la solución en la topología actúa como concentrador de todas las conexiones entre redes no confiables y los activos, entre los diferentes radios y entre otros accesos provenientes fuera de la solución.


---


- Identificador: I-BS.04

- Capa de Seguridad: Boundary Security

- Principio: Establecer controles con objeto de proteger la infraestructura y sus activos frente a amenazas cibernéticas del exterior.

- Objetivo: Establecer los mecanismos para asegurar y proteger el tráfico hacia las aplicaciones de negocio situándolas detrás de una puerta de enlace que evite la exposición directa de estas al exterior.

- Consideraciones al control:
    - Utilice las funcionalidades de proxy inverso sobre la red perimetral como medida para evitar la exposición directa de los activos hacia internet u otros enlaces al exterior.
    - Haga uso de las funcionalidades de proxy inverso en capa 7 para proteger y centralizar tanto la identidad como la integridad de los datos. Para ello, utilice las capacidades de content load balancing para tener control sobre el aislamiento de los servidores de aplicación, realice TLS offloading proporcionando visibilidad y cumplimiento (según los estándares de seguridad definidos), utilice la capa de autenticación para centralizar y proporcionar cumplimiento junto con las herramientas de autenticación, autorización y auditoría (AAA) tanto para una solución basada en B2C como B2B.
    - Haga uso de técnicas tales como multiplexing (multiplexación), isolation (aislamiento) y delaying como medida de reducir la exposición contra ataques de DoS o DDoS. Así también tenga en cuenta que deberá proporcionar funcionalidad de Dataguard (ofuscación y enmascaramiento) de cualquier dato sensible como datos personales o información sensible de tarjetas de crédito, entre otros.
    - Realice una implantación para aislar las diferentes cargas de trabajo, por ejemplo, mediante el uso de diferentes listeners (IPs virtuales) o virtual services (servicios virtuales). Así también implemente aislamiento y filtrado para los diferentes flujos, siendo estos flujos de FrontEnd y flujos de Backend, proporcionando así una solución de seguridad de doble capa de balanceo, ya sea mediante el uso de diferentes elementos virtuales o el uso de capacidades de multitenant.

---


- Identificador: I-BS.05

- Capa de Seguridad: Boundary Security

- Principio: Establecer controles con objeto de proteger la infraestructura y sus activos frente a amenazas cibernéticas del exterior.

- Objetivo: Asegurar que se establecen controles para proteger los datos contra exfiltraciones mediante el uso de herramientas o soluciones que permitan identificar y proteger los datos sensibles durante su movimiento. El requisito forma parte del objetivo general de proteger los datos contra exfiltraciones durante su procesamiento, movimiento o almacenamiento.

- Consideraciones al control:
    - El perímetro no deberá ser objeto del procesamiento o almacenamiento de datos sensibles, siendo parte de la política de aislamiento sobre zona desmilitarizada.
    - Deberá garantizar que todos los datos en tránsito dentro y fuera de la red perimetral hacen uso de mecanismos de cifrado, tales como TLS. A su vez, deberá garantizar que los mecanismos de cifrado utilizan versiones seguras y cifrados con alta entropía.
    - Haga uso de soluciones que permitan realizar TLS Offloading con objeto de monitorizar y proteger en el perímetro los datos tanto entrantes como salientes. Soluciones como RASP, WAF, API Protection, load balancers, etc. para tráfico entrante o proxies de navegación para tráfico saliente.
    - Deberá garantizar el ciclo de vida de los certificados o claves, incluida la creación e importación, la rotación, la revocación y el almacenamiento y su purga.
    - Los certificados/claves deberán cumplir el estándar definido sin usar propiedades no seguras, como un tamaño de clave insuficiente, un periodo de validez demasiado largo, criptografía no segura, entre otras.
    - Utilice certificados/claves firmados por una CA externa como Digicert o GlobalSign para todos los servicios expuestos hacia internet o mediante enlaces privados hacia terceros.
    - Asegúrese de establecer las medidas de seguridad del servicio de almacén de claves utilizado para la administración del ciclo de vida de las claves criptográficas y de los certificados.

---


- Identificador: I-BS.06

- Capa de Seguridad: Boundary Security

- Principio: Establecer controles con objeto de proteger la infraestructura y sus activos frente a amenazas cibernéticas del exterior.

- Objetivo: Desplegar soluciones con objeto de proteger los activos frente a denegaciones de servicios dirigidas.

- Consideraciones al control:
    - El perímetro deberá contar con las herramientas o soluciones que permitan proteger a los servicios frente a ataques de denegación de servicio en capas 3, 4 y 7 (según pila OSI). La solución deberá contar con protección DOS y DDoS (Distribuidos).

---


- Identificador: I-BS.07

- Capa de Seguridad: Boundary Security

- Principio: Establecer controles con objeto de proteger la infraestructura y sus activos frente a amenazas cibernéticas del exterior.

- Objetivo: Establecer mecanismos de protección contra malware que operen en tiempo real complementando los escaneos periódicos.

- Consideraciones al control:
    - Siempre y cuando los activos en la infraestructura cuenten con sistemas de protección de amenazas, se recomienda el uso de protección contra malware "al vuelo" sobre las capas perimetrales, haciendo uso de mecanismos como soluciones de SANDBOX dentro del módulo de threat prevention en los dispositivos de seguridad perimetral, o bien soluciones de protección de malware activas a nivel global sobre arquitecturas en entornos CLOUD.


---


- Identificador: I-BS.08

- Capa de Seguridad: Boundary Security

- Principio: Establecer controles con objeto de proteger la infraestructura y sus activos frente a amenazas cibernéticas del exterior.

- Objetivo: Hacer uso de herramientas que permitan identificar el tráfico legítimo del tráfico malicioso haciendo uso de herramientas automatizadas o semiautomatizadas (BOTs) como medida de proteger los activos frente a abuso, exfiltración, scraping, etc.

- Consideraciones al control:
    - Para flujos Norte-Sur con protocolo HTTP(s) cerciórese que estos atraviesan una solución de advanced Bot Defense (Antibot), Advanced L7 DDoS Protection (Protección sobre capa de aplicación para Denegación de Servicio Distribuido) o para tráfico API, soluciones como API Protection.
    - Las capacidades de Advanced Bot Defense deberán estar activadas para detectar, clasificar y proteger los activos frente a ataques producidos por Bots malintencionados. Para ello deberá aplicar tácticas tales como uso de FingerPrints, Secure-Cookies y JavaSripts. Además, deberá contar con una Bot Signature y la posibilidad de desplegar Security SDK, este último, que deberá implementarse sobre aplicaciones pesadas de escritorio o de dispositivos móviles.
    - Dichas protecciones deberán proporcionar mitigación frente a ataques de Credential Cracking, Account Creation, Search Abuse, shopping cart abuse, Checkout abuse, automated form submission, intellectual property harvesting, automated attack on Microservice, entre otras.
    - De idéntica forma, verifique que queda activa la protección frente a L7 DDoS proporcionando protección frente a ataques Volumétricos, computacionales, asimétricos, con base vulnerabilidad y distribuidos. Para ello active y establezca los mecanismos de protección basados en TPS (básico), heavy URL Protection (frente a ataques de estrés), behavioral DOS Protection (basados en el comportamiento ML), Geolocation (Geolocalización) y Client Reputation.


---


- Identificador: I-BS.09

- Capa de Seguridad: Boundary Security

- Principio: Establecer controles con objeto de proteger la infraestructura y sus activos frente a amenazas cibernéticas del exterior.

- Objetivo: Disponer y configurar las reglas necesarias en los cortafuegos de aplicaciones para proteger las aplicaciones web y APIs publicadas contra ataques específicos.

- Consideraciones al control:
    - Para los flujos Norte-Sur con protocolo HTTP(s) cerciórese que estos atraviesan una solución de Web Application Firewall (WAF) o RASP situada en el perímetro, con el objetivo de monitorizar y proteger los activos a nivel de aplicación.
    - Deberá cerciorarse de que el WAF o RASP trabaja en un modelo de seguridad negativa (Negative Security Model) mediante el uso de Attack Signatures y Threat Campaigns y en un modelo de seguridad positiva mediante la securización de cookies, parámetros estáticos y dinámicos tanto en el head como en el body, aplicando login enforcement, brute force Mitigation, tracking session, XML y SOA protection, URL and Flow control, API protection, entre otras.


---


- Identificador: I-BS.10

- Capa de Seguridad: Boundary Security

- Principio: Establecer controles con objeto de proteger la infraestructura y sus activos frente a amenazas cibernéticas del exterior.

- Objetivo: Hacer uso de herramientas y/o soluciones que permitan proteger el envío y recepción de correo, así como a la infraestructura que soporta el servicio, frente a ataques o amenazas del exterior.

- Consideraciones al control:
    - Hacer uso de controles de red para garantizar que el puerto saliente 25 solo queda habilitado para los remitentes de correo autorizados. Además, hacer uso de capacidades de IPS con medida de alertar de intentos no autorizados.
    - Deberá hacer uso de MSA (mail submission agent) internos confiables.
    - Será necesario acotar la exposición del puerto 25 SMTP entrante.
    - Se deberá implementar SPF con objeto de especificar qué direcciones IP están autorizadas para transmitir correo electrónico en nombre del dominio. Además, aquellos dominios los cuales no se hacen uso para el envío de correo electrónico deberán incluir un SPF RR con la política que indique que no hay remitentes de correo electrónico válidos para el determinado dominio.
    - Se deberá implementar DNSSEC, validando las respuestas destinadas a todos los sistemas receptores de correo electrónico. Además, deberá hacer uso de DNSSEC para proporcionar autenticación y protección de integridad de los registros DNS DKIM.
    - Deberá hacer uso de DMARC como base para ampliar la funcionalidad de seguridad de los protocolos SPF y DKIM.
    - Los buzones de correo no supervisados deben estar firmados digitalmente con firmas S/MIME para que los destinatarios puedan verificar la autenticidad de los mensajes.
    - Se hará uso del protocolo TLS con versiones y cifrados altos definidos en los estándares de ciberseguridad. Además, será necesario requerir autenticación de cadena de certificados contra una CA conocida.
    - Se deberá hacer uso de capacitación en seguridad de TI para los usuarios finales consumidores de correo electrónico.


---

- Identificador: I-BS.11

- Capa de Seguridad: Boundary Security

- Principio: Cumplir o mejorar con los valores técnicos de Resiliencia Tecnológica requeridos por el Grupo o las Líneas de Negocio Usuarias y reflejados en sus BIAs. Estos valores son: RTO, RPO y MBCO.

- Objetivo: Dotar a las infraestructuras soporte de los servicios Boundary Security de las medidas de Resiliencia Tecnológica necesarias para procurar la disponibilidad, confidencialidad e integridad de la información y servicios que estas provean, en función de los requisitos exigidos.

- Consideraciones al control:
    - Disponer de medidas de Resiliencia Tecnológica operativas que permitan cumplir con los valores técnicos, (RTO, RPO y MBCO), que se extraigan del análisis BIA de las mismas. En caso de que el servicio no disponga de BIA realizado y actualizado (antigüedad > 1 año), el responsable del proceso deberá solicitar su realización y la documentación de parámetros a Continuidad de Negocio Global.
    - Disponer de un plan de pruebas que verifique la operatividad de dichas medidas de Resiliencia Tecnológica y el cumplimiento de los valores técnicos recabados en los BIAS.
    - Disponer de un plan de mejoras que alineen los valores obtenidos con los demandados por negocio, si es que hubiera diferencias relevantes, o bien, la asunción del gap por parte del área gestora o negocio.



---


- Identificador: AP-ADL.01

- Capa de Seguridad: Application Security

- Principio: Establecer controles y procesos de desarrollo seguro durante todas las etapas del ciclo de vida del software.

- Objetivo: Garantizar que las aplicaciones cumplen con los requerimientos específicos en criterios de seguridad durante todo el ciclo de vida.

- Consideraciones al control:
    - Se deberá garantizar el cumplimiento de los requisitos del ciclo de vida del desarrollo seguro.
    - Verifique el uso del modelado de amenazas para cada cambio de diseño o planificación de sprints con el fin de identificarlas, planificar contramedidas, facilitar respuestas de riesgo adecuadas y guiar las pruebas de seguridad.
    - Verifique que todas las configuraciones de usuario y las funciones asignadas a cada uno de ellos contengan restricciones de seguridad funcionales. Ejemplo: "Como usuario, debería poder ver y editar mi perfil. No debería poder ver ni editar el perfil de otra persona".
    - Verifique la documentación y la justificación de todos los límites de confianza, componentes y flujos de datos importantes de la aplicación.
    - Verifique la definición y el análisis de seguridad de la arquitectura de alto nivel de la aplicación y todos los servicios remotos conectados.
    - Verifique la implementación de controles de seguridad centralizados, simples (economía de diseño), examinados, seguros y reutilizables para evitar controles duplicados, faltantes, ineficaces o inseguros.
    - Verifique la disponibilidad de una lista de verificación de codificación segura, requisitos de seguridad, pautas o políticas para todos los desarrolladores y analistas.


---


- Identificador: AP-AT.01

- Capa de Seguridad: Application Security

- Principio: Establecer las auditorías y análisis de seguridad en el código necesarias para su puesta y mantenimiento en producción.

- Objetivo: Garantizar que las aplicaciones cumplen con los requerimientos específicos en criterios de seguridad durante todo el ciclo de vida.

- Consideraciones al control:
    - Se deberán integrar todos los desarrollos con las plataformas y sistemas de versionado y análisis de código requeridas por la compañía.
    - El análisis SAST y SCA es requisito indispensable.
    - El análisis DAST no es de aplicación por defecto, puede ser requerido por la CISO Office.
    - El análisis RAST o Pentest de Red Team deberá realizarse según planificación y recursos del negocio, siendo siempre requisito indispensable previa puesta en producción.
    - Los sistemas requeridos como indispensables son el uso de repositorios en la plataforma de versionado e integración GITHUB de la compañía.
    - La realización de manera automatizada de tantos análisis estáticos como de componentes sea necesario mediante la herramienta Veracode.
    - La gestión, administración, implantación de requisitos, políticas y scores será definida por la CISO Office y DTI, quedando excluidas tales competencias a los negocios.


---

- Identificador: AP-API.01

- Capa de Seguridad: Application Security

- Principio: Establecer controles y procesos de desarrollo seguro que cumplan con todos los requerimientos para la no exposición a riesgos derivados de la integración con componentes y/o librerías de terceros, así como la integración y uso de API/SOA.

- Objetivo: Garantizar que las aplicaciones cumplen con los requerimientos específicos en criterios de seguridad durante todo el ciclo de vida.

- Consideraciones al control:
    - Se requiere el análisis de cuantos componentes o desarrollos de terceros formen parte del aplicativo. Se debe auditar y hacer uso de herramientas de análisis de código para la detección de código malicioso, como funciones de tiempo, operaciones de archivo inseguras y conexiones de red.
    - Verifique que el código fuente de la aplicación y las bibliotecas de terceros no contengan funciones no autorizadas de recopilación de datos de inicio. Cuando exista dicha funcionalidad, obtenga el permiso del usuario para que funcione antes de recopilar cualquier dato.
    - Se requiere la aplicabilidad del mínimo privilegio posible para cuantas funciones se realicen con componentes de terceros, al igual que la no integración de módulos, librerías y APIs cuyas funcionalidades no sean estrictamente necesarias. Verifique que la aplicación tenga límites de lógica de negocio o validación para proteger contra posibles riesgos o amenazas comerciales, identificados mediante el modelado de amenazas o metodologías similares.
    - Se requiere que la aplicación emplee protecciones de integridad, como la firma de código o la integridad de los recursos secundarios. La aplicación no debe cargar ni ejecutar código de fuentes que no sean de confianza, como cargar módulos, complementos, código o bibliotecas de fuentes que no hayan sido verificadas.
    - Se debe cumplir con los requisitos genéricos de verificación de seguridad del servicio web (SOAP, RestFul...).
    - Asegure el cumplimiento con la ley de protección de datos en el manejo y transacción de datos entre módulos, APIs o componentes de terceros.


---


- Identificador: AP-DSI.01

- Capa de Seguridad: Application Security

- Principio: Establecer controles y procesos de desarrollo seguro durante todas las etapas del ciclo de vida del software.

- Objetivo: Garantizar que las aplicaciones cumplen con los requerimientos específicos en criterios de seguridad durante todo el ciclo de vida.

- Consideraciones al control:
    - Se deberán cumplir con todas las normativas y requisitos para la implantación y puesta en producción de los aplicativos marcados por la compañía.
    - No se permitirá la exposición de entornos de desarrollo.
    - Se deberán aislar los desarrollos de cualquier sistema y base de datos en producción.
    - Para la consecución de pruebas y testing del aplicativo no podrán hacerse uso de bases de datos en producción y de datos reales de clientes y servicios.
    - Para la implantación de un entorno de desarrollo deberá cumplirse con todos los requisitos expuestos en la norma vigente.


---

- Identificador: AP-CO.01

- Capa de Seguridad: Application Security

- Principio: Establecer controles y procesos de desarrollo seguro para la generación de APKs y binarios ejecutables, tanto en infraestructura propia como de terceros.

- Objetivo: Garantizar que las aplicaciones cumplen con los requerimientos específicos que imposibiliten o dificulten la aplicación de técnicas de reversing sobre el código.

- Consideraciones al control:
    - Se requiere la aplicación de mecanismos de ofuscación y antireversing de todo el software generado por la compañía.
    - La ofuscación como proceso de transformación del código y datos con la finalidad de lograr hacerlos incomprensibles y difíciles de desensamblar.
    - Esta es una parte integral del esquema de protección del software.
    - Se pueden utilizar las siguientes técnicas para ofuscar una aplicación:
        - Ofuscación de nombres
        - Sustitución de instrucciones
        - Control sobre el flujo
        - Inyección de código muerto
        - Cifrado de cadenas
        - Compilado con funciones de antireversing

- Ejemplos para lenguaje C/C++:
    - Tanto GCC como Clang tienen opciones para ofuscar el código, como -fstack-protector, -fno-asynchronous-unwind-tables y -ffunction-sections. Microsoft Visual C++ y el Intel C++ Compiler también disponen de herramientas de ofuscación integradas.
    - Opciones de ofuscación integradas en GCC y Clang:
        - -fstack-protector: Agrega protección de desbordamiento de pila.
        - -fno-asynchronous-unwind-tables: Elimina las tablas de desenrollado asincrónico, lo que dificulta el análisis del flujo de control.
        - -ffunction-sections: Coloca cada función en su propia sección, lo que facilita la eliminación de código muerto.
        - -fdata-sections: Coloca cada variable en su propia sección, lo que también facilita la eliminación de código muerto.

    - Ofuscación de nombres:
        - gcc -fvisibility=hidden file.c -o file.o: Oculta la visibilidad de los símbolos.
        - clang -fvisibility=hidden file.c -o file.o: Opción similar en Clang.

    - Sustitución de instrucciones:
        - gcc -fno-asynchronous-unwind-tables file.c -o file.o: Elimina las tablas de desenrollado asincrónico.
        - clang -fno-asynchronous-unwind-tables file.c -o file.o: Opción similar en Clang.

    - Cambio de flujo:
        - gcc -ffunction-sections -fdata-sections file.c -o file.o: Separa funciones y variables en secciones.
        - clang -ffunction-sections -fdata-sections file.c -o file.o: Opción similar en Clang. Herramientas Adicionales: ProGuard, Obfuscator.NET, Obfuscator-llvm


---

- Identificador: AP-CCP.01

- Capa de Seguridad: Application Security

- Principio: Establecer procesos y configuraciones de seguridad sobre la parametrización y validación de datos, así como la gestión de los mismos.

- Objetivo: Garantizar que las aplicaciones cumplen con los requerimientos específicos en criterios de seguridad durante todo el ciclo de vida.

- Consideraciones al control:
    - Se deberá cumplir con requisitos de validación de entrada, sanitización y sandboxing.
    - Se deberá cumplir con los requisitos de codificación de salida y prevención de inyección.
    - Se requiere cumplir con requisitos de seguridad sobre el manejo de memoria, cadenas y código no administrado. Verifique que la aplicación utilice una cadena segura para la memoria, una copia de memoria más segura y aritmética de puntero para detectar o evitar desbordamientos de pila, búfer, etc.
    - Verifique que todas las entradas (campos de formulario HTML, solicitudes REST, parámetros de URL, encabezados HTTP, cookies, archivos por lotes, fuentes RSS, etc.) están validadas mediante validación positiva (listas de permitidos).
    - Se debe verificar que los marcos protegen contra ataques de asignación de parámetros masivos, o que la aplicación tenga contramedidas para proteger contra asignaciones de parámetros inseguras, como marcar campos como privados o similares.
    - Verifique que se utilicen técnicas de validación de signo, rango y entrada para evitar desbordamientos de enteros.
    - Verifique que la aplicación protege contra ataques SSRF, validando o desinfectando datos no confiables o metadatos de archivos HTTP, como nombres de archivos y campos de entrada de URL, y utiliza listas de permisos de protocolos, dominios, rutas y puertos.
    - Se deberá cumplir con los requisitos de prevención de deserialización, utilizando controles de integridad y cifrados.
    - Se debe cumplir con los requisitos de seguridad necesarios para los encabezados HTTP y la validación de los mismos.


---

- Identificador: AP-AR.01

- Capa de Seguridad: Application Security

- Principio: Establecer controles y procesos de desarrollo seguro durante todas las etapas del ciclo de vida del software.

- Objetivo: Garantizar que las aplicaciones cumplen con los requerimientos específicos en criterios de seguridad y recuperación durante todo el ciclo de vida productivo.

- Consideraciones al control:
    - Deberá cumplirse con todos los requisitos de contenido, procesamiento y protección de registros.
    - La aplicación deberá haber sido implementada con una correcta gestión de errores, como el manejo de excepciones en la totalidad del código o la muestra de mensajes genéricos al producirse un error inesperado.
    - Debe verificarse la implementación de backups automatizados según las políticas de la compañía, verificando la correcta restauración de los sistemas en caso de incidente.
    - Se deben implementar cuantos mecanismos de resiliencia sean necesarios.
    - Todos los archivos ejecutables y las bibliotecas que pertenecen a la aplicación están cifrados a nivel de archivo y/o el código importante y los segmentos de datos, dentro de los ejecutables, están cifrados o empaquetados. El análisis estático trivial no revela códigos o datos importantes.


---
- Identificador: M-IAM.01

- Capa de Seguridad: Identity and Access Management

- Principio: Proteger y asegurar el acceso a recursos y sistemas mediante un plano de gestión aislado del plano de datos o plano de servicio.

- Objetivo: Establecer medidas que permitan implementar un plano de gestión/control aislado del plano de servicio/datos para todos los recursos situados y componentes que conformen las soluciones, así como integrar los principios de acceso a la red.

- Consideraciones al control:
    - Gestionar los componentes de la infraestructura de la solución mediante un plano de gestión aislado del plano de datos.
    - En una infraestructura Cloud, garantizar que todas las operaciones de gestión se envían a la dirección URL de Azure Resource Manager para gestionar todas las solicitudes del plano del control que incluye control de acceso basado en roles, Azure Policy, bloqueos de administración y registros de actividad, además de uso de Azure for Cloud para el control de amenazas.
    - Para la gestión de Virtual Machines, utilizar Azure Bastion asegurando un principio de segmentación mediante control de tráfico hacia la red AzureBastionSubnet.
    - Almacenar las claves privadas de acceso en repositorio seguro, integrar con Azure AD para la administración de identidades y acceso global, hacer uso de RBAC, PIM e incluso PAW si el recurso en sí forma parte del Tier-0 y habilitar los registros de recursos de Azure Bastion.


---


- Identificador: M-IAM.02

- Capa de Seguridad: Identity and Access Management

- Principio: Proteger y asegurar el acceso a recursos y sistemas mediante la gestión segura de la identidad, garantizando el uso de una capa adicional de seguridad en los inicios de sesión.

- Objetivo: Establecer controles para asegurar y proteger el acceso a recursos y sistemas mediante la gestión segura de la identidad, incluyendo inicio de sesión únicos, mecanismos robustos de autenticación, administración de las identidades, inicios de servicios, acceso a aplicaciones y la supervisión de accesos condicionales y las anomalías en cuentas.

- Consideraciones al control:
    - Reforzar los mecanismos de acceso a los recursos para garantizar inicios de sesión únicos.
    - Asegurar el uso de mecanismos y protocolos de autenticación robustos.
    - Emplear políticas de control de acceso basadas en identidad, roles y atributos, así como mecanismos de aplicación de acceso como listas de control de acceso, matrices de control de acceso, cifrado.
    - Establecer mecanismos de autorización de accesos a información considerada clasificada y segmentarla por niveles.


---

- Identificador: M-IAM.03

- Capa de Seguridad: Identity and Access Management

- Principio: Asegurar que se otorgan niveles de autorización requeridos según el principio del mínimo privilegio, en los sistemas y aplicaciones de la compañía.

- Objetivo: Establecer los procedimientos y controles para asegurar que se otorgan los permisos y niveles de acceso adecuados para el desempeño de las funciones y asegurando los principios de Least Privilege.

- Consideraciones al control:
    - Implementar controles de acceso granular para garantizar que los usuarios y sistemas solo tengan acceso a los recursos y datos necesarios para realizar sus funciones autorizadas.
    - Establecer mecanismos para asignar los permisos a usuarios autorizados y los procedimientos necesarios para administrar los permisos.


---


- Identificador: M-IAM.04

- Capa de Seguridad: Identity and Access Management

- Principio: Establecer controles para registrar, analizar y reportar la administración de identidades y acceso.

- Objetivo: Garantizar que se implementen procesos adecuados para registrar eventos relevantes, analizar los registros de estos eventos para detectar anomalías y posibles amenazas, reportar hallazgos y tendencias de seguridad relacionados con la administración de identidades y acceso a los sistemas, aplicaciones, servicios e infraestructura.

- Consideraciones al control:
    - Detectar amenazas para la administración de identidades y acceso mediante la supervisión del inicio de sesión y el acceso de usuarios y aplicaciones. Se deben alertar patrones de comportamiento tales como el número excesivo de intentos de inicio de sesión con errores y las cuentas en desuso de la suscripción.
    - Habilitar el registro de los recursos en la nube para cumplir con los requisitos de investigación de incidentes y respuestas de seguridad y cumplimiento normativo.
    - Habilitar el registro de los servicios de red para admitir las investigaciones de incidentes relacionadas con la red, la búsqueda de amenazas y la generación de alertas de seguridad.

---

- Identificador: M-IAM.05

- Capa de Seguridad: Identity and Access Management

- Principio: Gestionar de forma centralizada la identificación, autenticación y el ciclo de vida de los usuarios, mediante mecanismos adecuados de Gestión de Identidades.

- Objetivo: Establecer controles para asegurar y proteger el acceso a recursos y sistemas mediante la gestión segura de la identidad, administración de las identidades, acceso a aplicaciones y la supervisión de todo el ciclo integral de vida de los usuarios hasta su baja.

- Consideraciones al control:
    - Proteger el sistema de identidad y autenticación.
    - Administrar las identidades de aplicaciones de forma segura y automática.
    - Autenticar servidores y servicios.
    - Hacer uso de inicio de sesión único para el acceso a las aplicaciones.
    - Hacer uso de controles de autenticación sólida.
    - Restringir el acceso a los recursos en función de las condiciones.
    - Restringir la exposición de credenciales y secretos.


---

- Identificador: M-IAM.06

- Capa de Seguridad: Identity and Access Management

- Principio: Realizar una gestión eficaz y segura de identidades y accesos en el entorno corporativo a través de sistemas centralizados.

- Objetivo: Establecer políticas, procedimientos y controles adecuados para administrar de manera segura y efectiva las identidades de usuario y los privilegios de acceso a los recursos en las diferentes infraestructuras de la compañía.

- Consideraciones al control:
    - Establecer políticas de gestión de identidades y acceso.
    - Implementar controles de acceso basados en roles (RBAC).
    - Aplicar la autenticación y la autorización de forma adecuada: esto puede incluir el uso de autenticación multifactor (MFA), la integración con servicios de directorio como Azure Active Directory (AAD) y la configuración de políticas de autorización granular.

---

- Identificador: M-IAM.07

- Capa de Seguridad: Identity and Access Management

- Principio: Proteger y asegurar las cuentas de administración a través del control exhaustivo de sus accesos y privilegios dentro del entorno corporativo.

- Objetivo: Establecer controles para asegurar que el acceso a servicios, cuentas y herramientas de administración de entornos y sistemas se gestionan (configuran, otorgan, retiran y supervisan) de forma segura y adecuada.

- Consideraciones al control:
    - Identificar las cuentas de alto impacto y limitar el número de cuentas administrativas o con privilegios elevados en el plano de control, plano de administración y plano de datos.
    - Usar mecanismos de Just-In-Time para asignar acceso con privilegios a los distintos niveles de recursos.
    - Usar un proceso automatizado para administrar el ciclo de vida de identidades y acceso.
    - Revisar periódicamente los derechos de las cuentas privilegiadas.
    - Configurar un acceso de emergencia para asegurar que no quede bloqueado por accidente de la infraestructura. Estas cuentas deberán guardarse bajo llave y solo ciertas personas de la organización deberán tener acceso a ellas.
    - Seguir el principio de administración suficiente para administrar los permisos en un nivel específico. Utilizar para ello control de acceso basado en roles y/o acceso basado en atributos.


---

- Identificador: M-IAM.08

- Capa de Seguridad: Identity and Access Management

- Principio: Fortalecer la seguridad de las identidades de usuarios y los mecanismos de autenticación para brindar acceso a recursos corporativos.

- Objetivo: Aplicar controles de autenticación sólida (autenticación sólida sin contraseña o autenticación multifactor) con el sistema de administración de identidades y autenticación.

- Consideraciones al control:
    - Establecer procesos robustos para gestionar los accesos privilegiados en la administración de los recursos corporativos.
    - Aplicar autenticación multifactor (MFA) para accesos privilegiados.

---


- Identificador: M-IAM.09

- Capa de Seguridad: Identity and Access Management

- Principio: Garantizar la seguridad de los secretos de las aplicaciones utilizadas para autenticar y autorizar aplicaciones y servicios en el entorno corporativo.

- Objetivo: Establecer un sistema de gestión de credenciales centralizado que permita la gestión del ciclo de vida de las credenciales de la entidad utilizadas para la autenticación, esto incluye usuario/password, public y private keys, valores biométricos, etc.

- Consideraciones al control:
    - Almacenamiento seguro de secretos: Se debe utilizar un mecanismo seguro para almacenar y gestionar los secretos de la aplicación y servicios de gestión de secretos disponibles en Azure.
    - Gestión de accesos y permisos: Se deben aplicar controles de acceso y permisos adecuados para limitar el acceso a los secretos de la aplicación solo a usuarios y servicios autorizados.
    - Rotación regular de secretos: Se debe implementar un proceso para rotar regularmente los secretos de la aplicación, como contraseñas y claves API, para reducir el riesgo de compromiso debido a la exposición prolongada.

---


- Identificador: M-IAM.10

- Capa de Seguridad: Identity and Access Management

- Principio: Garantizar la protección adecuada de los datos relacionados con la identidad y el acceso contra la divulgación, manipulación o acceso no autorizado.

- Objetivo: Garantizar el cumplimiento de las políticas asociadas a la gestión de accesos e identidades, por ejemplo, aquellas asociadas a los niveles de autorización, sesiones de acceso múltiple, tiempo de actividad del sistema, identificación y autenticación de usuarios, fortaleza de la autenticación, etc.

- Consideraciones al control:
    - Encriptación de datos sensibles, para ello se deben aplicar técnicas de cifrado sobre datos de identidad y acceso, tanto en reposo como en tránsito.
    - Aplicar controles de acceso y permisos adecuados solo a usuarios y servicios autorizados.
    - Implementar un proceso seguro para la gestión de claves de cifrado utilizadas para proteger las identidades y accesos tanto en la nube como on-premise.

---


- Identificador: M-IAM.11

- Capa de Seguridad: Identity and Access Management

- Principio: Garantizar la seguridad de las comunicaciones y la autenticación en sistemas y redes que hacen uso de infraestructuras de clave pública (PKI).

- Objetivo: Proteger adecuadamente la información de autenticación, incluyendo las claves públicas y privadas utilizadas en una infraestructura de clave pública.

- Consideraciones al control:
    - Definir y gestionar las políticas y tecnologías que garanticen la protección de comunicaciones que hacen uso de certificados digitales de PKI.
    - Automatización de los ciclos de creación, renovación y revocación de los certificados emitidos por la PKI y gestión de estos.


---

- Identificador: M-IAM.02

- Capa de Seguridad: Identity and Access Management

- Principio: Proteger y asegurar el acceso a recursos y sistemas mediante la gestión segura de la identidad, garantizando el uso de una capa adicional de seguridad en los inicios de sesión.

- Objetivo: Establecer controles para asegurar y proteger el acceso a recursos y sistemas mediante la gestión segura de la identidad, incluyendo inicio de sesión únicos, mecanismos robustos de autenticación, administración de las identidades, inicios de servicios, acceso a aplicaciones y la supervisión de accesos condicionales y las anomalías en cuentas.

- Consideraciones al control:
    - Reforzar los mecanismos de acceso a los recursos para garantizar inicios de sesión únicos.
    - Asegurar el uso de mecanismos y protocolos de autenticación robustos.
    - Emplear políticas de control de acceso basadas en identidad, roles y atributos, así como mecanismos de aplicación de acceso como listas de control de acceso, matrices de control de acceso, cifrado.
    - Establecer mecanismos de autorización de accesos a información considerada clasificada y segmentarla por niveles.

---


- Identificador: M-IAM.02

- Capa de Seguridad: Identity and Access Management

- Principio: Proteger y asegurar el acceso a recursos y sistemas mediante la gestión segura de la identidad, garantizando el uso de una capa adicional de seguridad en los inicios de sesión.

- Objetivo: Establecer controles para asegurar y proteger el acceso a recursos y sistemas mediante la gestión segura de la identidad, incluyendo inicio de sesión únicos, mecanismos robustos de autenticación, administración de las identidades, inicios de servicios, acceso a aplicaciones y la supervisión de accesos condicionales y las anomalías en cuentas.

- Consideraciones al control:
    - Reforzar los mecanismos de acceso a los recursos para garantizar inicios de sesión únicos.
    - Asegurar el uso de mecanismos y protocolos de autenticación robustos.
    - Emplear políticas de control de acceso basadas en identidad, roles y atributos, así como mecanismos de aplicación de acceso como listas de control de acceso, matrices de control de acceso, cifrado.
    - Establecer mecanismos de autorización de accesos a información considerada clasificada y segmentarla por niveles.

---


- Identificador: M-IAM.02

- Capa de Seguridad: Identity and Access Management

- Principio: Proteger y asegurar el acceso a recursos y sistemas mediante la gestión segura de la identidad, garantizando el uso de una capa adicional de seguridad en los inicios de sesión.

- Objetivo: Establecer controles para asegurar y proteger el acceso a recursos y sistemas mediante la gestión segura de la identidad, incluyendo inicio de sesión únicos, mecanismos robustos de autenticación, administración de las identidades, inicios de servicios, acceso a aplicaciones y la supervisión de accesos condicionales y las anomalías en cuentas.

- Consideraciones al control:
    - Reforzar los mecanismos de acceso a los recursos para garantizar inicios de sesión únicos.
    - Asegurar el uso de mecanismos y protocolos de autenticación robustos.
    - Emplear políticas de control de acceso basadas en identidad, roles y atributos, así como mecanismos de aplicación de acceso como listas de control de acceso, matrices de control de acceso, cifrado.
    - Establecer mecanismos de autorización de accesos a información considerada clasificada y segmentarla por niveles.

---

- Identificador: AI-SMLC.01

- Capa de Seguridad: MLOps AI Security

- Principio: Se debe crear, implementar y mantener sistemas de aprendizaje automático (ML) de manera confiable y eficiente. Puede hacerse esto utilizando el proceso de MLOps, que es una combinación de DevOps, ingeniería de datos y técnicas de ML.

- Objetivo: MLOps proporciona un enfoque sistemático para evaluar y monitorear modelos de ML. MLOps se ocupa de la gestión del ciclo de vida de los proyectos de ML. Esto implica entrenar, implementar y mantener modelos de aprendizaje automático para garantizar la eficiencia. La seguridad es un componente esencial de todas las etapas del ciclo de vida de MLOps. Garantiza que todo el ciclo de vida cumpla con los estándares requeridos.

- Consideraciones al control:
    - Aplicar todos los controles y requisitos de seguridad en el desarrollo que garanticen la protección de al menos el top 10 de amenazas de OWASP para MLOps:
        - ML01:2023 Ataque de manipulación de entrada
        - ML02:2023 Ataque de envenenamiento de datos
        - ML03:2023 Ataque de inversión de modelo
        - ML04:2023 Ataque de inferencia de membresía
        - ML05:2023 Robo de modelos
        - ML06:2023 Ataques a la cadena de suministro de IA
        - ML07:2023 Ataque de transferencia de aprendizaje
        - ML08:2023 Modelo sesgado
        - ML09:2023 Ataque a la integridad de la salida
        - ML10:2023 Envenenamiento de modelos

---

- Identificador: AI-SDC.01

- Capa de Seguridad: MLOps AI Security

- Principio: Proteger el almacenamiento de datos, comprender las políticas de cumplimiento de datos, proteger los modelos de ML, garantizar la observabilidad y registrar las tareas de ML contribuyen en gran medida a proteger MLOps.

- Objetivo: Los datos son un aporte importante en el entrenamiento de modelos de ML. Una forma eficaz de proteger los modelos de aprendizaje automático es comprender los datos utilizados para entrenar el modelo, de dónde provienen y qué contienen.

- Consideraciones al control:
    - Se debe asegurar el cumplimiento de las leyes de protección de datos y de propiedad intelectual a la hora de obtener y hacer uso de bases de datos para entrenar modelos de ML, sobre todo en el caso de utilizar datos confidenciales o privados.
    - Debe comprender las leyes de su jurisdicción en relación con el manejo y almacenamiento de datos. Es requisito indispensable la valoración por el departamento legal de la compañía. (enmascaramiento, cifrado, protección de bases de datos)
    - Verificar la calidad y precisión de los datos de origen antes de entrenar un modelo de ML.

---


- Identificador: AI-SDM.01

- Capa de Seguridad: MLOps AI Security

- Principio: Proteger el almacenamiento de datos, comprender las políticas de cumplimiento de datos, proteger los modelos de ML, garantizar la observabilidad y registrar las tareas de ML contribuyen en gran medida a proteger MLOps.

- Objetivo: Debe evitar obtener sus datos de capacitación de conjuntos de datos que no sean de confianza y al mismo tiempo seguir los procedimientos estándar de detección y mitigación de seguridad de datos. Los datos envenenados ponen en duda la confiabilidad y confidencialidad de sus datos y, en última instancia, el modelo de ML.

- Consideraciones al control:
    - Es posible que un modelo entrenado con datos manipulados no genere predicciones precisas. Un atacante puede aplicar ingeniería inversa a un modelo de aprendizaje automático, replicarlo y explotarlo para obtener beneficios personales. Si esto sucede, debe identificar las muestras de datos deficientes de su modelo, eliminarlas y volver a entrenar el modelo original antes del ataque.
    - Se deben bloquear los intentos de ataque y detectar entradas maliciosas mediante limitación de velocidad, verificación de validez, pruebas de regresión, etc. La limitación de velocidad controla la frecuencia con la que un usuario puede repetir una actividad.
    - Realice pruebas de regresión para ayudar a prevenir errores de ML al realizar un seguimiento del rendimiento del modelo de ML.
    - Se deben realizar ataques simulados contra sus algoritmos para aprender cómo construir defensas contra ataques de envenenamiento de datos.

---


- Identificador: AI-MO.01

- Capa de Seguridad: MLOps AI Security

- Principio: Establecer controles con objeto de garantizar la disponibilidad y recuperación de los datos sobre los endpoints.

- Objetivo: Un modelo entrenado, implementado y monitoreado mediante el método MLOps es rastreable de un extremo a otro. Este método registra el linaje del modelo para rastrear su origen. Esto significa que puede rastrear fácilmente el código fuente y los datos utilizados para entrenar y probar el modelo. Además, proteger el almacenamiento de datos, comprender las políticas de cumplimiento de datos, proteger los modelos de ML, garantizar la observabilidad y registrar las tareas de ML contribuyen en gran medida a proteger MLOps.

- Consideraciones al control:
    - Debe registrar cada evento en el almacenamiento de datos para saber qué sucede cada vez que hay una actividad. Los archivos de registro contienen una pista de auditoría que puede utilizar para monitorear las actividades dentro del almacenamiento de datos.
    - Se deben supervisar los registros para evitar intrusiones ilícitas en los sistemas de almacenamiento de datos. Requisito indispensable para la realización de una investigación forense tras una violación de seguridad.
    - Es obligatorio cumplir con todos los requisitos y controles para una auditoría. Es importante para proteger el sistema de almacenamiento de datos contra amenazas externas y el mal uso interno de la información.