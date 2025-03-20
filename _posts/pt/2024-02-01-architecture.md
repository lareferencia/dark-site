---
layout: post
title:  "Arquitetura e Componentes"  
date:   2024-02-01 00:00:00 +0200  
description:  "Arquitetura e Componentes"  
language: pt  
language_reference: architecture
categories: post
published: true
---


A arquitetura do sistema dARK é projetada com uma clara separação de componentes, organizados em Camada de Serviço e Camada Central.

<img src="{{ site.baseurl }}/assets/img/architecture.png" alt="Diagrama de Arquitetura dARK" class="img-fluid mb-4" />

<h2 class="custom-heading">Camada de Serviço</h2>

A Camada de Serviço fornece serviços essenciais que interagem com os componentes da Camada Central. Esses serviços incluem:

<div class="service-components">
  <div class="service-item">
    <h4><a href="https://github.com/dARKf3n1Xx/dark-resolver" target="_blank">dARK Resolver</a></h4>
    <p>Integrado com o sistema global de resolução nt2.info, permitindo a resolução de identificadores persistentes</p>
    <div class="code-access">
      <a href="https://github.com/dARKf3n1Xx/dark-resolver" target="_blank">Acesse o código-fonte no GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><a href="https://github.com/dARKf3n1Xx/dark-minter" target="_blank">dARK Minter</a></h4>
    <p>Usado para criar e registrar novos PIDs no sistema</p>
    <div class="code-access">
      <a href="https://github.com/dARKf3n1Xx/dark-minter" target="_blank">Acesse o código-fonte no GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><a href="https://github.com/dARKf3n1Xx/dark-dashboard" target="_blank">dARK Dashboard</a></h4>
    <p>Fornece recursos de monitoramento e administração para a plataforma</p>
    <div class="code-access">
      <a href="https://github.com/dARKf3n1Xx/dark-dashboard" target="_blank">Acesse o código-fonte no GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><a href="https://github.com/dARKf3n1Xx/dark-api" target="_blank">dARK API</a></h4>
    <p>Facilita a comunicação entre aplicações e o blockchain subjacente</p>
    <div class="code-access">
      <a href="https://github.com/dARKf3n1Xx/dark-api" target="_blank">Acesse o código-fonte no GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><a href="https://github.com/dARKf3n1Xx/dark-backup" target="_blank">dARK Backup</a></h4>
    <p>Garante a durabilidade dos dados e a confiabilidade do sistema</p>
    <div class="code-access">
      <a href="https://github.com/dARKf3n1Xx/dark-backup" target="_blank">Acesse o código-fonte no GitHub</a>
    </div>
  </div>

  <div class="service-item">
    <h4><a href="https://github.com/dARKf3n1Xx/dark-backup" target="_blank">dARK LA Referencia</a></h4>
    <p>Implementa a criação em massa de dARK na Plataforma Coletora LA Referencia</p>
    <div class="code-access">
      <a href="https://github.com/dARKf3n1Xx/dark-backup" target="_blank">Acesse o código-fonte no GitHub</a>
    </div>
  </div>
</div>

Esses serviços são suportados por mecanismos de balanceamento de carga para garantir alta disponibilidade e desempenho ótimo do sistema.

<h2 class="custom-heading">Camada Central (dARK dApp)</h2>

A Camada Central é construída sobre uma rede blockchain permissionada que forma a espinha dorsal do sistema dARK. Em seu núcleo está uma rede pública permissionada operando com um mecanismo de consenso de Prova de Autoridade (PoA), fornecendo segurança e eficiência para o gerenciamento de PIDs.

<div class="service-item core-app">
  <h4><a href="https://github.com/dARKf3n1Xx/dark-dapp" target="_blank">dARK dApp</a></h4>
  <p>Aplicação descentralizada central que implementa os contratos inteligentes de gerenciamento de PID e garante a integridade dos dados através da tecnologia blockchain</p>
  <div class="code-access">
    <a href="https://github.com/dARKf3n1Xx/dark-dapp" target="_blank">Acesse o código-fonte no GitHub</a>
  </div>
</div>

<h3 class="custom-heading-secondary">Fundação Blockchain</h3>

A rede utiliza a tecnologia <a href="https://besu.hyperledger.org/" target="_blank">Hyperledger Besu</a> para fornecer uma base blockchain segura e eficiente. O Hyperledger Besu é um cliente Ethereum projetado para uso empresarial que suporta implantações de rede permissionada tanto públicas quanto privadas. Sua implementação da Máquina Virtual Ethereum (EVM) permite contratos inteligentes sofisticados que gerenciam operações de PID com total transparência e auditabilidade.

<h3 class="custom-heading-secondary">Arquitetura de Rede</h3>

Projetada com resiliência e confiabilidade como princípios fundamentais, a arquitetura começa com uma **Rede dARK Mínima Viável (MVDN)**. Esta rede consiste em nós blockchain essenciais que fornecem a funcionalidade fundamental necessária para a operação do sistema. Esses nós gerenciam comunicações RPC/API e mantêm o livro-razão distribuído de identificadores persistentes. Cada nó completo implementa endpoints de API para interação de serviços externos através de balanceamento de carga.

Para garantir operação contínua mesmo durante falhas de nós, a arquitetura incorpora redundância tolerante a falhas através de nós de backup e sistemas de replicação de dados. Esta abordagem distribuída garante que nenhum ponto único de falha possa comprometer a integridade ou disponibilidade da infraestrutura PID.

<h3 class="custom-heading-secondary">Camada de Aplicação</h3>

Na camada de aplicação, o dARK dApp oferece a funcionalidade central para gerenciar identificadores persistentes através de contratos inteligentes. Esta lógica de aplicação lida com a criação, atualização e resolução de PIDs, aplicando regras de governança definidas pelos participantes da rede.

<div class="architecture-details">
  <div class="detail-box">
    <h4>Infraestrutura Federada</h4>
    <p>A arquitetura suporta múltiplas redes blockchain independentes operadas por diferentes autoridades, criando uma infraestrutura PID verdadeiramente federada.</p>
  </div>
  
  <div class="detail-box">
    <h4>Design Escalável</h4>
    <p>O sistema pode escalar horizontalmente adicionando mais nós à rede, garantindo alto desempenho mesmo com números crescentes de PIDs.</p>
  </div>
  
  <div class="detail-box">
    <h4>Extensões Futuras</h4>
    <p>O design modular permite a incorporação futura de soluções de armazenamento adicionais, como IPFS, para cargas de metadados maiores, mantendo a integridade dos dados através de verificação criptográfica na cadeia.</p>
  </div>
</div>

<h2 class="custom-heading">Integração com o Ecossistema</h2>

O sistema dARK é projetado para se integrar perfeitamente ao ecossistema acadêmico existente, particularmente com redes de repositórios, periódicos diamante e agregadores de metadados, seguindo este fluxo de trabalho inicial:

<div class="workflow-container">
  <div class="workflow-step">
    <div class="step-number">1</div>
    <div class="step-content">
      <h4>Coleta de Metadados</h4>
      <p>Agregadores coletam regularmente metadados de repositórios institucionais, periódicos e outros provedores de conteúdo através de protocolos padrão como OAI-PMH ou APIs personalizadas.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">2</div>
    <div class="step-content">
      <h4>Atribuição de PID</h4>
      <p>Para conteúdo sem identificadores persistentes, o agregador pode solicitar novos ARKs através da API do dARK Minter. Para ARKs existentes, eles são validados e registrados no sistema dARK.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">3</div>
    <div class="step-content">
      <h4>Registro no Blockchain</h4>
      <p>O sistema dARK registra cada ARK no blockchain, juntamente com sua URL de destino e metadados essenciais, fornecendo um registro descentralizado e à prova de adulteração dos identificadores.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">4</div>
    <div class="step-content">
      <h4>Distribuição de PID</h4>
      <p>Os ARKs recém-criados ou validados podem ser enviados de volta aos repositórios para inclusão em seus registros de metadados, permitindo uma abordagem padronizada para identificação persistente em toda a rede.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">5</div>
    <div class="step-content">
      <h4>Resolução</h4>
      <p>Quando um usuário acessa um ARK, o resolvedor global redireciona para o resolvedor dARK, que usa o blockchain para recuperar as informações de localização atuais, garantindo acesso persistente mesmo quando as localizações dos recursos mudam.</p>
    </div>
  </div>
</div>

Esta abordagem de integração permite que agregadores de metadados como LA Referencia aprimorem seus serviços com infraestrutura de PID descentralizada, preservando fluxos de trabalho existentes e agregando valor à rede de repositórios como um todo. Também permite transições perfeitas quando repositórios movem conteúdo ou mudam de plataformas, pois o sistema de resolução de PID pode ser atualizado sem quebrar links externos.

<div class="note-container">
  <div class="note-header">
    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#8A3691" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <circle cx="12" cy="12" r="10"></circle>
      <line x1="12" y1="8" x2="12" y2="12"></line>
      <line x1="12" y1="16" x2="12.01" y2="16"></line>
    </svg>
    <h4>Desenvolvimento Futuro</h4>
  </div>
  <div class="note-content">
    <p>Nas próximas fases de desenvolvimento, o projeto dARK planeja:</p>
    <ul>
      <li>Transformar este projeto inicial (atualmente em funcionamento no IBICT/Brasil) em um serviço regional abrangente projetado como uma infraestrutura pública, seguindo os princípios estabelecidos pela LA Referencia</li>
      <li>Desenvolver plugins para os sistemas de repositório e periódicos mais amplamente utilizados para facilitar a integração perfeita com a infraestrutura dARK</li>
      <li>Implementar persistência de metadados descentralizada para preservar informações bibliográficas e servir como fonte de dados confiável para sistemas analíticos como OpenAlex</li>
    </ul>
    <p>Esses aprimoramentos fortalecerão ainda mais o ecossistema dARK e expandirão sua utilidade dentro do panorama de comunicação acadêmica na América Latina e além.</p>
  </div>
</div>





