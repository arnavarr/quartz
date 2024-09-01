





<div style="border: 2px solid #4CAF50; border-radius: 10px; padding: 15px; background-color: rgba(255, 255, 255, 0); box-shadow: 2px 2px 12px rgba(0, 0, 0, 0.1); max-width: 600px; margin: 20px auto; font-weight: bold;">
    <p><strong>Identificador:</strong> <code>I-BS.04</code></p>
    <p><strong>Capa de Seguridad:</strong> Boundary Security</p>
    <p><strong>Principio:</strong> Establecer controles con objeto de proteger la infraestructura y sus activos frente a amenazas cibernéticas del exterior.</p>
    <p><strong>Objetivo:</strong> Establecer los mecanismos para asegurar y proteger el tráfico hacia las aplicaciones de negocio situándolas detrás de una puerta de enlace que evite la exposición directa de estas al exterior.</p>

    <h3 style="color: #4CAF50;">Consideraciones al Control</h3>
    <ul style="padding-left: 20px;">
        <li>Utilice las funcionalidades de proxy inverso sobre la red perimetral como medida para evitar la exposición directa de los activos hacia internet u otros enlaces al exterior.</li>
        <li>Haga uso de las funcionalidades de proxy inverso en capa 7 para proteger y centralizar tanto la identidad como la integridad de los datos. Para ello, utilice las capacidades de content load balancing para tener control sobre el aislamiento de los servidores de aplicación, realice TLS offloading proporcionando visibilidad y cumplimiento (según los estándares de seguridad definidos), utilice la capa de autenticación para centralizar y proporcionar cumplimiento junto con las herramientas de autenticación, autorización y auditoría (AAA) tanto para una solución basada en B2C como B2B.</li>
        <li>Haga uso de técnicas tales como multiplexing (multiplexación), isolation (aislamiento) y delaying como medida de reducir la exposición contra ataques de DoS o DDoS. Así también tenga en cuenta que deberá proporcionar funcionalidad de Dataguard (ofuscación y enmascaramiento) de cualquier dato sensible como datos personales o información sensible de tarjetas de crédito, entre otros.</li>
        <li>Realice una implantación para aislar las diferentes cargas de trabajo, por ejemplo, mediante el uso de diferentes listeners (IPs virtuales) o virtual services (servicios virtuales). Así también implemente aislamiento y filtrado para los diferentes flujos, siendo estos flujos de FrontEnd y flujos de Backend, proporcionando así una solución de seguridad de doble capa de balanceo, ya sea mediante el uso de diferentes elementos virtuales o el uso de capacidades de multitenant.</li>
    </ul>
</div>

<div style="border: 2px solid #4CAF50; border-radius: 10px; padding: 15px; background-color: rgba(255, 255, 255, 0); box-shadow: 2px 2px 12px rgba(0, 0, 0, 0.1); max-width: 600px; margin: 20px auto; font-weight: bold;">
    <p><strong>Identificador:</strong> <code>I-BS.05</code></p>
    <p><strong>Capa de Seguridad:</strong> Boundary Security</p>
    <p><strong>Principio:</strong> Establecer controles con objeto de proteger la infraestructura y sus activos frente a amenazas cibernéticas del exterior.</p>
    <p><strong>Objetivo:</strong> Asegurar que se establecen controles para proteger los datos contra exfiltraciones mediante el uso de herramientas o soluciones que permitan identificar y proteger los datos sensibles durante su movimiento. El requisito forma parte del objetivo general de proteger los datos contra exfiltraciones durante su procesamiento, movimiento o almacenamiento.</p>

    <h3 style="color: #4CAF50;">Consideraciones al Control</h3>
    <ul style="padding-left: 20px;">
        <li>El perímetro no deberá ser objeto del procesamiento o almacenamiento de datos sensibles, siendo parte de la política de aislamiento sobre zona desmilitarizada.</li>
        <li>Deberá garantizar que todos los datos en tránsito dentro y fuera de la red perimetral hacen uso de mecanismos de cifrado, tales como TLS. A su vez, deberá garantizar que los mecanismos de cifrado utilizan versiones seguras y cifrados con alta entropía.</li>
        <li>Haga uso de soluciones que permitan realizar TLS Offloading con objeto de monitorizar y proteger en el perímetro los datos tanto entrantes como salientes. Soluciones como RASP, WAF, API Protection, load balancers, etc. para tráfico entrante o proxies de navegación para tráfico saliente.</li>
        <li>Deberá garantizar el ciclo de vida de los certificados o claves, incluida la creación e importación, la rotación, la revocación y el almacenamiento y su purga.</li>
        <li>Los certificados/claves deberán cumplir el estándar definido sin usar propiedades no seguras, como un tamaño de clave insuficiente, un periodo de validez demasiado largo, criptografía no segura, entre otras.</li>
        <li>Utilice certificados/claves firmados por una CA externa como Digicert o GlobalSign para todos los servicios expuestos hacia internet o mediante enlaces privados hacia terceros.</li>
        <li>Asegúrese de establecer las medidas de seguridad del servicio de almacén de claves utilizado para la administración del ciclo de vida de las claves criptográficas y de los certificados.</li>
    </ul>
</div>

























<div style="border: 2px solid #4CAF50; border-radius: 10px; padding: 15px; background-color: rgba(255, 255, 255, 0); box-shadow: 2px 2px 12px rgba(0, 0, 0, 0.1); max-width: 600px; margin: 20px auto; font-weight: bold;">
    <p><strong>Identificador:</strong> <code>AI-SMLC.01</code></p>
    <p><strong>Capa de Seguridad:</strong> MLOps AI Security</p>
    <p><strong>Principio:</strong> Se debe crear, implementar y mantener sistemas de aprendizaje automático (ML) de manera confiable y eficiente. Puede hacerse esto utilizando el proceso de MLOps, que es una combinación de DevOps, ingeniería de datos y técnicas de ML.</p>
    <p><strong>Objetivo:</strong> MLOps proporciona un enfoque sistemático para evaluar y monitorear modelos de ML. MLOps se ocupa de la gestión del ciclo de vida de los proyectos de ML. Esto implica entrenar, implementar y mantener modelos de aprendizaje automático para garantizar la eficiencia. La seguridad es un componente esencial de todas las etapas del ciclo de vida de MLOps. Garantiza que todo el ciclo de vida cumpla con los estándares requeridos.</p>

    <h3 style="color: #4CAF50;">Consideraciones al Control</h3>
    <ul style="padding-left: 20px;">
        <li>Aplicar todos los controles y requisitos de seguridad en el desarrollo que garanticen la protección de al menos el top 10 de amenazas de OWASP para MLOps:
            <ul>
                <li>ML01:2023 Ataque de manipulación de entrada</li>
                <li>ML02:2023 Ataque de envenenamiento de datos</li>
                <li>ML03:2023 Ataque de inversión de modelo</li>
                <li>ML04:2023 Ataque de inferencia de membresía</li>
                <li>ML05:2023 Robo de modelos</li>
                <li>ML06:2023 Ataques a la cadena de suministro de IA</li>
                <li>ML07:2023 Ataque de transferencia de aprendizaje</li>
                <li>ML08:2023 Modelo sesgado</li>
                <li>ML09:2023 Ataque a la integridad de la salida</li>
                <li>ML10:2023 Envenenamiento de modelos</li>
            </ul>
        </li>
    </ul>
</div>

<div style="border: 2px solid #4CAF50; border-radius: 10px; padding: 15px; background-color: rgba(255, 255, 255, 0); box-shadow: 2px 2px 12px rgba(0, 0, 0, 0.1); max-width: 600px; margin: 20px auto; font-weight: bold;">
    <p><strong>Identificador:</strong> <code>AI-SDC.01</code></p>
    <p><strong>Capa de Seguridad:</strong> MLOps AI Security</p>
    <p><strong>Principio:</strong> Proteger el almacenamiento de datos, comprender las políticas de cumplimiento de datos, proteger los modelos de ML, garantizar la observabilidad y registrar las tareas de ML contribuyen en gran medida a proteger MLOps.</p>
    <p><strong>Objetivo:</strong> Los datos son un aporte importante en el entrenamiento de modelos de ML. Una forma eficaz de proteger los modelos de aprendizaje automático es comprender los datos utilizados para entrenar el modelo, de dónde provienen y qué contienen.</p>

    <h3 style="color: #4CAF50;">Consideraciones al Control</h3>
    <ul style="padding-left: 20px;">
        <li>Se debe asegurar el cumplimiento de las leyes de protección de datos y de propiedad intelectual a la hora de obtener y hacer uso de bases de datos para entrenar modelos de ML, sobre todo en el caso de utilizar datos confidenciales o privados.</li>
        <li>Debe comprender las leyes de su jurisdicción en relación con el manejo y almacenamiento de datos. Es requisito indispensable la valoración por el departamento legal de la compañía. (enmascaramiento, cifrado, protección de bases de datos)</li>
        <li>Verificar la calidad y precisión de los datos de origen antes de entrenar un modelo de ML.</li>
    </ul>
</div>

<div style="border: 2px solid #4CAF50; border-radius: 10px; padding: 15px; background-color: rgba(255, 255, 255, 0); box-shadow: 2px 2px 12px rgba(0, 0, 0, 0.1); max-width: 600px; margin: 20px auto; font-weight: bold;">
    <p><strong>Identificador:</strong> <code>AI-SDM.01</code></p>
    <p><strong>Capa de Seguridad:</strong> MLOps AI Security</p>
    <p><strong>Principio:</strong> Proteger el almacenamiento de datos, comprender las políticas de cumplimiento de datos, proteger los modelos de ML, garantizar la observabilidad y registrar las tareas de ML contribuyen en gran medida a proteger MLOps.</p>
    <p><strong>Objetivo:</strong> Debe evitar obtener sus datos de capacitación de conjuntos de datos que no sean de confianza y al mismo tiempo seguir los procedimientos estándar de detección y mitigación de seguridad de datos. Los datos envenenados ponen en duda la confiabilidad y confidencialidad de sus datos y, en última instancia, el modelo de ML.</p>

    <h3 style="color: #4CAF50;">Consideraciones al Control</h3>
    <ul style="padding-left: 20px;">
        <li>Es posible que un modelo entrenado con datos manipulados no genere predicciones precisas. Un atacante puede aplicar ingeniería inversa a un modelo de aprendizaje automático, replicarlo y explotarlo para obtener beneficios personales. Si esto sucede, debe identificar las muestras de datos deficientes de su modelo, eliminarlas y volver a entrenar el modelo original antes del ataque.</li>
        <li>Se deben bloquear los intentos de ataque y detectar entradas maliciosas mediante limitación de velocidad, verificación de validez, pruebas de regresión, etc. La limitación de velocidad controla la frecuencia con la que un usuario puede repetir una actividad.</li>
        <li>Realice pruebas de regresión para ayudar a prevenir errores de ML al realizar un seguimiento del rendimiento del modelo de ML.</li>
        <li>Se deben realizar ataques simulados contra sus algoritmos para aprender cómo construir defensas contra ataques de envenenamiento de datos.</li>
    </ul>
</div>

<div style="border: 2px solid #4CAF50; border-radius: 10px; padding: 15px; background-color: rgba(255, 255, 255, 0); box-shadow: 2px 2px 12px rgba(0, 0, 0, 0.1); max-width: 600px; margin: 20px auto; font-weight: bold;">
    <p><strong>Identificador:</strong> <code>AI-MO.01</code></p>
    <p><strong>Capa de Seguridad:</strong> MLOps AI Security</p>
    <p><strong>Principio:</strong> Establecer controles con objeto de garantizar la disponibilidad y recuperación de los datos sobre los endpoints.</p>
    <p><strong>Objetivo:</strong> Un modelo entrenado, implementado y monitoreado mediante el método MLOps es rastreable de un extremo a otro. Este método registra el linaje del modelo para rastrear su origen. Esto significa que puede rastrear fácilmente el código fuente y los datos utilizados para entrenar y probar el modelo. Además, proteger el almacenamiento de datos, comprender las políticas de cumplimiento de datos, proteger los modelos de ML, garantizar la observabilidad y registrar las tareas de ML contribuyen en gran medida a proteger MLOps.</p>

    <h3 style="color: #4CAF50;">Consideraciones al Control</h3>
    <ul style="padding-left: 20px;">
        <li>Debe registrar cada evento en el almacenamiento de datos para saber qué sucede cada vez que hay una actividad. Los archivos de registro contienen una pista de auditoría que puede utilizar para monitorear las actividades dentro del almacenamiento de datos.</li>
        <li>Se deben supervisar los registros para evitar intrusiones ilícitas en los sistemas de almacenamiento de datos. Requisito indispensable para la realización de una investigación forense tras una violación de seguridad.</li>
        <li>Es obligatorio cumplir con todos los requisitos y controles para una auditoría. Es importante para proteger el sistema de almacenamiento de datos contra amenazas externas y el mal uso interno de la información.</li>
    </ul>
</div>
