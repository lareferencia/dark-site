---
layout: post
title:  "Arquitectura y Componentes"  
date:   2024-02-01 00:00:00 +0200  
description:  "Arquitectura y Componentes"  
language: es  
language_reference: architecture
categories: post
published: true
---


La arquitectura del sistema dARK está diseñada con una clara separación de componentes, organizados en la Capa de Servicio y la Capa Core.

<img src="{{ site.baseurl }}/assets/img/architecture.png" alt="Diagrama de Arquitectura dARK" class="img-fluid mb-4" />

<h2 class="custom-heading">Capa de Servicio</h2>

La Capa de Servicio proporciona servicios esenciales que interactúan con los componentes de la Capa Core. Estos servicios incluyen:

<div class="service-components">
  <div class="service-item">
    <h4><a href="https://github.com/dARKf3n1Xx/dark-resolver" target="_blank">dARK Resolver</a></h4>
    <p>Integrado con el sistema de resolución global nt2.info, permitiendo la resolución de identificadores persistentes</p>
    <div class="code-access">
      <a href="https://github.com/dARKf3n1Xx/dark-resolver" target="_blank">Acceder al código fuente en GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><a href="https://github.com/dARKf3n1Xx/dark-minter" target="_blank">dARK Minter</a></h4>
    <p>Utilizado para crear y registrar nuevos PIDs en el sistema</p>
    <div class="code-access">
      <a href="https://github.com/dARKf3n1Xx/dark-minter" target="_blank">Acceder al código fuente en GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><a href="https://github.com/dARKf3n1Xx/dark-dashboard" target="_blank">dARK Dashboard</a></h4>
    <p>Proporciona capacidades de monitoreo y administración para la plataforma</p>
    <div class="code-access">
      <a href="https://github.com/dARKf3n1Xx/dark-dashboard" target="_blank">Acceder al código fuente en GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><a href="https://github.com/dARKf3n1Xx/dark-api" target="_blank">dARK API</a></h4>
    <p>Facilita la comunicación entre aplicaciones y la blockchain subyacente</p>
    <div class="code-access">
      <a href="https://github.com/dARKf3n1Xx/dark-api" target="_blank">Acceder al código fuente en GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><a href="https://github.com/dARKf3n1Xx/dark-backup" target="_blank">dARK Backup</a></h4>
    <p>Asegura la durabilidad de los datos y la confiabilidad del sistema</p>
    <div class="code-access">
      <a href="https://github.com/dARKf3n1Xx/dark-backup" target="_blank">Acceder al código fuente en GitHub</a>
    </div>
  </div>

  <div class="service-item">
    <h4><a href="https://github.com/dARKf3n1Xx/dark-backup" target="_blank">dARK LA Referencia</a></h4>
    <p>Implementa la acuñación masiva de dARK en la Plataforma de Recolección de LA Referencia</p>
    <div class="code-access">
      <a href="https://github.com/dARKf3n1Xx/dark-backup" target="_blank">Acceder al código fuente en GitHub</a>
    </div>
  </div>
</div>

Estos servicios son respaldados por mecanismos de balanceo de carga para garantizar alta disponibilidad y rendimiento óptimo del sistema.

<h2 class="custom-heading">Capa Core (dARK dApp)</h2>

La Capa Core está construida sobre una red blockchain permisionada que forma la columna vertebral del sistema dARK. En su núcleo hay una red pública permisionada que opera con un mecanismo de consenso de Prueba de Autoridad (PoA), proporcionando tanto seguridad como eficiencia para la gestión de PIDs.

<div class="service-item core-app">
  <h4><a href="https://github.com/dARKf3n1Xx/dark-dapp" target="_blank">dARK dApp</a></h4>
  <p>Aplicación descentralizada central que implementa los contratos inteligentes de gestión de PID y asegura la integridad de los datos mediante tecnología blockchain</p>
  <div class="code-access">
    <a href="https://github.com/dARKf3n1Xx/dark-dapp" target="_blank">Acceder al código fuente en GitHub</a>
  </div>
</div>

<h3 class="custom-heading-secondary">Fundamentos de Blockchain</h3>

La red aprovecha la tecnología <a href="https://besu.hyperledger.org/" target="_blank">Hyperledger Besu</a> para proporcionar una base blockchain segura y eficiente. Hyperledger Besu es un cliente Ethereum diseñado para uso empresarial que soporta implementaciones de redes permisionadas tanto públicas como privadas. Su implementación de la Máquina Virtual Ethereum (EVM) permite contratos inteligentes sofisticados que gestionan operaciones de PID con total transparencia y auditabilidad.

<h3 class="custom-heading-secondary">Arquitectura de Red</h3>

Diseñada con la resiliencia y la confiabilidad como principios fundamentales, la arquitectura comienza con una **Red dARK Mínima Viable (MVDN)**. Esta red consiste en nodos blockchain esenciales que proporcionan la funcionalidad fundamental requerida para la operación del sistema. Estos nodos gestionan las comunicaciones RPC/API y mantienen el libro contable distribuido de identificadores persistentes. Cada nodo completo implementa endpoints API para la interacción de servicios externos a través del balanceo de carga.

Para garantizar la operación continua incluso durante fallos de nodos, la arquitectura incorpora redundancia tolerante a fallos mediante nodos de respaldo y sistemas de replicación de datos. Este enfoque distribuido asegura que ningún punto único de fallo pueda comprometer la integridad o disponibilidad de la infraestructura PID.

<h3 class="custom-heading-secondary">Capa de Aplicación</h3>

En la capa de aplicación, la dARK dApp ofrece la funcionalidad central para gestionar identificadores persistentes a través de contratos inteligentes. Esta lógica de aplicación maneja la creación, actualización y resolución de PIDs mientras hace cumplir las reglas de gobernanza definidas por los participantes de la red.

<div class="architecture-details">
  <div class="detail-box">
    <h4>Infraestructura Federada</h4>
    <p>La arquitectura soporta múltiples redes blockchain independientes operadas por diferentes autoridades, creando una infraestructura PID verdaderamente federada.</p>
  </div>
  
  <div class="detail-box">
    <h4>Diseño Escalable</h4>
    <p>El sistema puede escalar horizontalmente añadiendo más nodos a la red, asegurando alto rendimiento incluso con números crecientes de PIDs.</p>
  </div>
  
  <div class="detail-box">
    <h4>Extensiones Futuras</h4>
    <p>El diseño modular permite la incorporación futura de soluciones de almacenamiento adicionales como IPFS para cargas de metadatos más grandes, manteniendo la integridad de los datos a través de verificación criptográfica en la cadena.</p>
  </div>
</div>

<h2 class="custom-heading">Integración con el Ecosistema</h2>

El sistema dARK está diseñado para integrarse perfectamente con el ecosistema académico existente, particularmente con redes de repositorios, revistas diamond y agregadores de metadatos, siguiendo este flujo de trabajo inicial:

<div class="workflow-container">
  <div class="workflow-step">
    <div class="step-number">1</div>
    <div class="step-content">
      <h4>Recolección de Metadatos</h4>
      <p>Los agregadores recolectan regularmente metadatos de repositorios institucionales, revistas y otros proveedores de contenido a través de protocolos estándar como OAI-PMH o APIs personalizadas.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">2</div>
    <div class="step-content">
      <h4>Asignación de PID</h4>
      <p>Para contenido sin identificadores persistentes, el agregador puede solicitar nuevos ARKs a través de la API de dARK Minter. Para ARKs existentes, son validados y registrados en el sistema dARK.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">3</div>
    <div class="step-content">
      <h4>Registro en Blockchain</h4>
      <p>El sistema dARK registra cada ARK en la blockchain, junto con su URL de destino y metadatos esenciales, proporcionando un registro descentralizado y a prueba de manipulaciones de los identificadores.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">4</div>
    <div class="step-content">
      <h4>Distribución de PID</h4>
      <p>Los ARKs recién acuñados o validados pueden ser enviados de vuelta a los repositorios para su inclusión en sus registros de metadatos, permitiendo un enfoque estandarizado para la identificación persistente en toda la red.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">5</div>
    <div class="step-content">
      <h4>Resolución</h4>
      <p>Cuando un usuario accede a un ARK, el resolvedor global redirige al resolvedor dARK, que utiliza la blockchain para recuperar la información de ubicación actual, asegurando acceso persistente incluso cuando cambian las ubicaciones de los recursos.</p>
    </div>
  </div>
</div>

Este enfoque de integración permite a agregadores de metadatos como LA Referencia mejorar sus servicios con infraestructura PID descentralizada mientras preservan los flujos de trabajo existentes y añaden valor a la red de repositorios en su conjunto. También permite transiciones fluidas cuando los repositorios mueven contenido o cambian de plataformas, ya que el sistema de resolución de PID puede actualizarse sin romper enlaces externos.

<div class="note-container">
  <div class="note-header">
    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#8A3691" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <circle cx="12" cy="12" r="10"></circle>
      <line x1="12" y1="8" x2="12" y2="12"></line>
      <line x1="12" y1="16" x2="12.01" y2="16"></line>
    </svg>
    <h4>Desarrollo Futuro</h4>
  </div>
  <div class="note-content">
    <p>En las próximas fases de desarrollo, el proyecto dARK planea:</p>
    <ul>
      <li>Transformar este proyecto inicial (actualmente funcionando en IBICT/Brasil) en un servicio regional integral diseñado como infraestructura pública, siguiendo los principios establecidos por LA Referencia</li>
      <li>Desarrollar plugins para los sistemas de repositorios y revistas más utilizados para facilitar la integración perfecta con la infraestructura dARK</li>
      <li>Implementar persistencia de metadatos descentralizada para preservar información bibliográfica y servir como fuente de datos confiable para sistemas analíticos como OpenAlex</li>
    </ul>
    <p>Estas mejoras fortalecerán aún más el ecosistema dARK y expandirán su utilidad dentro del panorama de comunicación académica en América Latina y más allá.</p>
  </div>
</div>





