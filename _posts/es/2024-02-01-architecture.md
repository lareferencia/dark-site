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
    <h4><a href="https://github.com/dark-pid/dark-resolver" target="_blank">dARK Resolver</a></h4>
    <p>Integrado con el sistema global de resolución nt2.info, permitiendo la resolución de identificadores persistentes</p>
    <div class="code-access">
      <a href="https://github.com/dark-pid/dark-resolver" target="_blank">Acceder al código fuente en GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><a href="https://github.com/dark-pid/hyperdrive" target="_blank">dARK Minter</a></h4>
    <p>Utilizado para crear y registrar nuevos PIDs en el sistema</p>
    <div class="code-access">
      <a href="https://github.com/dark-pid/hyperdrive" target="_blank">Acceder al código fuente en GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><span class="disabled-link">dARK Dashboard</span></h4>
    <p>Proporciona capacidades de monitoreo y administración para la plataforma</p>
    <div class="code-access">
      <span class="disabled-link">Acceder al código fuente en GitHub</span>
    </div>
  </div>
  
  <div class="service-item">
    <h4><a href="https://github.com/dark-pid/dark-gateway" target="_blank">dARK API</a></h4>
    <p>Facilita la comunicación entre aplicaciones y la blockchain subyacente</p>
    <div class="code-access">
      <a href="https://github.com/dark-pid/dark-gateway" target="_blank">Acceder al código fuente en GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><span class="disabled-link">dARK Backup</span></h4>
    <p>Garantiza la durabilidad de los datos y la fiabilidad del sistema</p>
    <div class="code-access">
      <span class="disabled-link">Acceder al código fuente en GitHub</span>
    </div>
  </div>

  <div class="service-item">
    <h4><a href="https://github.com/lareferencia/lareferencia-dark-lib" target="_blank">dARK LA Referencia</a></h4>
    <p>Implementa la creación masiva de dARK en la Plataforma de Cosecha de LA Referencia</p>
    <div class="code-access">
      <a href="https://github.com/lareferencia/lareferencia-dark-lib" target="_blank">Acceder al código fuente en GitHub</a>
    </div>
  </div>
</div>

Estos servicios están respaldados por mecanismos de balanceo de carga para garantizar alta disponibilidad y un rendimiento óptimo del sistema.

<h2 class="custom-heading">Capa Core (dARK dApp)</h2>

La Capa Core está construida sobre una red blockchain con permisos que forma la columna vertebral del sistema dARK. En su núcleo se encuentra una red pública con permisos que opera con un mecanismo de consenso de Prueba de Autoridad (PoA), proporcionando tanto seguridad como eficiencia para la gestión de PIDs.

<div class="disclaimer-box">
  <div class="disclaimer-icon">
    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#8A3691" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M10.29 3.86L1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z"></path>
      <line x1="12" y1="9" x2="12" y2="13"></line>
      <line x1="12" y1="17" x2="12.01" y2="17"></line>
    </svg>
  </div>
  <div class="disclaimer-content">
    <h4>Sobre la madurez de código abierto dARK</h4>
    <p> dARK es un proyecto de código abierto y está disponible para la comunidad global de Ciencia Abierta. Sin embargo, es un proyecto en constante evolución, prueba y mejora. Por lo tanto, no recomendamos crear implementaciones de producción basadas de dARK en este momento. Estamos abiertos a contribuciones de código y pruebas en entornos piloto, y alentamos la participación de la comunidad a través de estos canales.</p>
  </div>
</div>

<div class="service-item core-app">
  <h4><a href="https://github.com/dark-pid/dARK" target="_blank">dARK dApp</a></h4>
  <p>Aplicación descentralizada central que implementa los contratos inteligentes de gestión de PIDs y garantiza la integridad de los datos a través de la tecnología blockchain</p>
  <div class="code-access">
    <a href="https://github.com/dark-pid/dARK" target="_blank">Acceder al código fuente en GitHub</a>
  </div>
</div>

<h3 class="custom-heading-secondary">Fundación Blockchain</h3>

La red aprovecha la tecnología <a href="https://besu.hyperledger.org/" target="_blank">Hyperledger Besu</a> para proporcionar una base blockchain segura y eficiente. Hyperledger Besu es un cliente de Ethereum diseñado para uso empresarial que admite implementaciones de redes públicas y privadas con permisos. Su implementación de la Máquina Virtual de Ethereum (EVM) permite contratos inteligentes sofisticados que gestionan operaciones de PID con total transparencia y auditabilidad.

<h3 class="custom-heading-secondary">Arquitectura de la Red</h3>

Diseñada con la resiliencia y la fiabilidad como principios fundamentales, la arquitectura comienza con una **Red dARK Mínima Viable (MVDN)**. Esta red consta de nodos blockchain esenciales que proporcionan la funcionalidad fundamental requerida para la operación del sistema. Estos nodos gestionan las comunicaciones RPC/API y mantienen el libro mayor distribuido de identificadores persistentes. Cada nodo completo implementa puntos finales de API para la interacción de servicios externos a través de balanceo de carga.

Para garantizar la operación continua incluso durante fallos de nodos, la arquitectura incorpora redundancia tolerante a fallos a través de nodos de respaldo y sistemas de replicación de datos. Este enfoque distribuido asegura que ningún punto único de fallo pueda comprometer la integridad o disponibilidad de la infraestructura de PID.

<h3 class="custom-heading-secondary">Capa de Aplicación</h3>

En la capa de aplicación, la dARK dApp ofrece la funcionalidad central para gestionar identificadores persistentes a través de contratos inteligentes. Esta lógica de aplicación maneja la creación, actualización y resolución de PIDs mientras aplica las reglas de gobernanza definidas por los participantes de la red.

<div class="architecture-details">
  <div class="detail-box">
    <h4>Infraestructura Federada</h4>
    <p>La arquitectura admite múltiples redes blockchain independientes operadas por diferentes autoridades, creando una infraestructura de PID verdaderamente federada.</p>
  </div>
  
  <div class="detail-box">
    <h4>Diseño Escalable</h4>
    <p>El sistema puede escalar horizontalmente añadiendo más nodos a la red, asegurando un alto rendimiento incluso con un número creciente de PIDs.</p>
  </div>
  
  <div class="detail-box">
    <h4>Extensiones Futuras</h4>
    <p>El diseño modular permite la incorporación futura de soluciones de almacenamiento adicionales como IPFS para cargas de metadatos más grandes, manteniendo la integridad de los datos a través de la verificación criptográfica en la cadena.</p>
  </div>
</div>

<h2 class="custom-heading">Integración del Ecosistema</h2>

El sistema dARK está diseñado para integrarse sin problemas con el ecosistema académico existente, particularmente con redes de repositorios, revistas diammond y agregadores de metadatos, siguiendo este flujo de trabajo inicial:

<div class="workflow-container">
  <div class="workflow-step">
    <div class="step-number">1</div>
    <div class="step-content">
      <h4>Cosecha de Metadatos</h4>
      <p>Los agregadores cosechan regularmente metadatos de repositorios institucionales, revistas y otros proveedores de contenido a través de protocolos estándar como OAI-PMH o APIs personalizadas.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">2</div>
    <div class="step-content">
      <h4>Asignación de PID</h4>
      <p>Para contenido sin identificadores persistentes, el agregador puede solicitar nuevos ARKs a través de la API de dARK Minter. Para ARKs existentes, se validan y registran en el sistema dARK.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">3</div>
    <div class="step-content">
      <h4>Registro en Blockchain</h4>
      <p>El sistema dARK registra cada ARK en la blockchain, junto con su URL de destino y metadatos esenciales, proporcionando un registro descentralizado y a prueba de manipulaciones de identificadores.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">4</div>
    <div class="step-content">
      <h4>Distribución de PID</h4>
      <p>Los ARKs recién creados o validados pueden ser enviados de vuelta a los repositorios para su inclusión en sus registros de metadatos, permitiendo un enfoque estandarizado para la identificación persistente en toda la red.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">5</div>
    <div class="step-content">
      <h4>Resolución</h4>
      <p>Cuando un usuario accede a un ARK, el resolver global redirige al resolver dARK, que utiliza la blockchain para recuperar la información de ubicación actual, asegurando el acceso persistente incluso cuando cambian las ubicaciones de los recursos.</p>
    </div>
  </div>
</div>

Este enfoque de integración permite a los agregadores de metadatos como LA Referencia mejorar sus servicios con una infraestructura de PID descentralizada mientras preservan los flujos de trabajo existentes y agregan valor a la red de repositorios en su conjunto. También permite transiciones sin problemas cuando los repositorios mueven contenido o cambian de plataforma, ya que el sistema de resolución de PID puede actualizarse sin romper enlaces externos.

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
      <li>Transformar este proyecto inicial (actualmente trabajando en IBICT/Brasil) en un servicio regional integral diseñado como una infraestructura pública, siguiendo los principios establecidos por LA Referencia</li>
      <li>Desarrollar plugins para los sistemas de repositorios y revistas más utilizados para facilitar la integración sin problemas con la infraestructura dARK</li>
      <li>Implementar persistencia descentralizada de metadatos para preservar la información bibliográfica y servir como una fuente de datos confiable para sistemas analíticos como OpenAlex</li>
    </ul>
    <p>Estas mejoras fortalecerán aún más el ecosistema dARK y expandirán su utilidad dentro del panorama de la comunicación académica en toda América Latina y más allá.</p>
  </div>
</div>

<style>
.disabled-link {
  color: #333;
  font-weight: 500;
  cursor: default;
  text-decoration: none;
}

.disclaimer-box {
  display: flex;
  background-color: #f8f4f9;
  border-left: 4px solid #8A3691;
  padding: 1rem;
  margin: 1.5rem 0;
  border-radius: 0 4px 4px 0;
}

.disclaimer-icon {
  flex-shrink: 0;
  margin-right: 1rem;
  display: flex;
  align-items: flex-start;
}

.disclaimer-content {
  flex-grow: 1;
}

.disclaimer-content h4 {
  margin-top: 0;
  margin-bottom: 0.5rem;
  color: #8A3691;
}

.disclaimer-content p {
  margin-bottom: 0;
  font-size: 0.95rem;
  line-height: 1.5;
}
</style>





