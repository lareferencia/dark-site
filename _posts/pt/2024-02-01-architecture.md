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


A arquitetura do sistema dARK é projetada com uma clara separação de componentes, organizados na Camada de Serviço e na Camada Core.

<img src="{{ site.baseurl }}/assets/img/architecture.png" alt="Diagrama de Arquitetura dARK" class="img-fluid mb-4" />

<h2 class="custom-heading">Camada de Serviço</h2>

A Camada de Serviço fornece serviços essenciais que interagem com os componentes da Camada Core. Estes serviços incluem:

<div class="service-components">
  <div class="service-item">
    <h4><a href="https://github.com/dark-pid/dark-resolver" target="_blank">dARK Resolver</a></h4>
    <p>Integrado com o sistema global de resolução nt2.info, permitindo a resolução de identificadores persistentes</p>
    <div class="code-access">
      <a href="https://github.com/dark-pid/dark-resolver" target="_blank">Acessar o código fonte no GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><a href="https://github.com/dark-pid/hyperdrive" target="_blank">dARK Minter</a></h4>
    <p>Utilizado para criar e registrar novos PIDs no sistema</p>
    <div class="code-access">
      <a href="https://github.com/dark-pid/hyperdrive" target="_blank">Acessar o código fonte no GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><span class="disabled-link">dARK Dashboard</span></h4>
    <p>Fornece capacidades de monitoramento e administração para a plataforma</p>
    <div class="code-access">
      <span class="disabled-link">Acessar o código fonte no GitHub</span>
    </div>
  </div>
  
  <div class="service-item">
    <h4><a href="https://github.com/dark-pid/dark-gateway" target="_blank">dARK API</a></h4>
    <p>Facilita a comunicação entre aplicações e o blockchain subjacente</p>
    <div class="code-access">
      <a href="https://github.com/dark-pid/dark-gateway" target="_blank">Acessar o código fonte no GitHub</a>
    </div>
  </div>
  
  <div class="service-item">
    <h4><span class="disabled-link">dARK Backup</span></h4>
    <p>Garante a durabilidade dos dados e a confiabilidade do sistema</p>
    <div class="code-access">
      <span class="disabled-link">Acessar o código fonte no GitHub</span>
    </div>
  </div>

  <div class="service-item">
    <h4><a href="https://github.com/lareferencia/lareferencia-dark-lib" target="_blank">dARK LA Referencia</a></h4>
    <p>Implementa a criação massiva de dARK na Plataforma de Colheita da LA Referencia</p>
    <div class="code-access">
      <a href="https://github.com/lareferencia/lareferencia-dark-lib" target="_blank">Acessar o código fonte no GitHub</a>
    </div>
  </div>
</div>

Estes serviços são apoiados por mecanismos de balanceamento de carga para garantir alta disponibilidade e um desempenho ótimo do sistema.

<h2 class="custom-heading">Camada Core (dARK dApp)</h2>

A Camada Core é construída sobre uma rede blockchain com permissões que forma a coluna vertebral do sistema dARK. Em seu núcleo está uma rede pública com permissões que opera com um mecanismo de consenso de Prova de Autoridade (PoA), proporcionando tanto segurança quanto eficiência para a gestão de PIDs.

<div class="disclaimer-box">
  <div class="disclaimer-icon">
    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#8A3691" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M10.29 3.86L1.82 18a2 2 0 0 0 1.71 3h16.94a2 2 0 0 0 1.71-3L13.71 3.86a2 2 0 0 0-3.42 0z"></path>
      <line x1="12" y1="9" x2="12" y2="13"></line>
      <line x1="12" y1="17" x2="12.01" y2="17"></line>
    </svg>
  </div>
  <div class="disclaimer-content">
    <h4>Sobre a maturidade do código aberto dARK</h4>
    <p>dARK é um projeto de código aberto e está disponível para a comunidade global de Ciência Aberta. No entanto, é um projeto em constante evolução, teste e melhoria. Portanto, não recomendamos criar implementações de produção baseadas em dARK neste momento. Estamos abertos a contribuições de código e testes em ambientes piloto, e encorajamos a participação da comunidade através desses canais.</p>
  </div>
</div>

<div class="service-item core-app">
  <h4><a href="https://github.com/dark-pid/dARK" target="_blank">dARK dApp</a></h4>
  <p>Aplicação descentralizada central que implementa os contratos inteligentes de gestão de PIDs e garante a integridade dos dados através da tecnologia blockchain</p>
  <div class="code-access">
    <a href="https://github.com/dark-pid/dARK" target="_blank">Acessar o código fonte no GitHub</a>
  </div>
</div>

<h3 class="custom-heading-secondary">Fundação Blockchain</h3>

A rede aproveita a tecnologia <a href="https://besu.hyperledger.org/" target="_blank">Hyperledger Besu</a> para fornecer uma base blockchain segura e eficiente. Hyperledger Besu é um cliente Ethereum projetado para uso empresarial que suporta implementações de redes públicas e privadas com permissões. Sua implementação da Máquina Virtual Ethereum (EVM) permite contratos inteligentes sofisticados que gerenciam operações de PID com total transparência e auditabilidade.

<h3 class="custom-heading-secondary">Arquitetura da Rede</h3>

Projetada com a resiliência e a confiabilidade como princípios fundamentais, a arquitetura começa com uma **Rede dARK Mínima Viável (MVDN)**. Esta rede consiste em nós blockchain essenciais que fornecem a funcionalidade fundamental necessária para a operação do sistema. Estes nós gerenciam as comunicações RPC/API e mantêm o livro-razão distribuído de identificadores persistentes. Cada nó completo implementa endpoints de API para a interação de serviços externos através de balanceamento de carga.

Para garantir a operação contínua mesmo durante falhas de nós, a arquitetura incorpora redundância tolerante a falhas através de nós de backup e sistemas de replicação de dados. Esta abordagem distribuída assegura que nenhum ponto único de falha possa comprometer a integridade ou disponibilidade da infraestrutura de PID.

<h3 class="custom-heading-secondary">Camada de Aplicação</h3>

Na camada de aplicação, o dARK dApp oferece a funcionalidade central para gerenciar identificadores persistentes através de contratos inteligentes. Esta lógica de aplicação gerencia a criação, atualização e resolução de PIDs enquanto aplica as regras de governança definidas pelos participantes da rede.

<div class="architecture-details">
  <div class="detail-box">
    <h4>Infraestrutura Federada</h4>
    <p>A arquitetura suporta múltiplas redes blockchain independentes operadas por diferentes autoridades, criando uma infraestrutura de PID verdadeiramente federada.</p>
  </div>
  
  <div class="detail-box">
    <h4>Design Escalável</h4>
    <p>O sistema pode escalar horizontalmente adicionando mais nós à rede, assegurando um alto desempenho mesmo com um número crescente de PIDs.</p>
  </div>
  
  <div class="detail-box">
    <h4>Extensões Futuras</h4>
    <p>O design modular permite a incorporação futura de soluções de armazenamento adicionais como IPFS para cargas de metadados maiores, mantendo a integridade dos dados através da verificação criptográfica na cadeia.</p>
  </div>
</div>

<h2 class="custom-heading">Integração do Ecossistema</h2>

O sistema dARK é projetado para se integrar perfeitamente com o ecossistema acadêmico existente, particularmente com redes de repositórios, revistas diamond e agregadores de metadados, seguindo este fluxo de trabalho inicial:

<div class="workflow-container">
  <div class="workflow-step">
    <div class="step-number">1</div>
    <div class="step-content">
      <h4>Colheita de Metadados</h4>
      <p>Os agregadores coletam regularmente metadados de repositórios institucionais, revistas e outros provedores de conteúdo através de protocolos padrão como OAI-PMH ou APIs personalizadas.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">2</div>
    <div class="step-content">
      <h4>Atribuição de PID</h4>
      <p>Para conteúdo sem identificadores persistentes, o agregador pode solicitar novos ARKs através da API do dARK Minter. Para ARKs existentes, são validados e registrados no sistema dARK.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">3</div>
    <div class="step-content">
      <h4>Registro no Blockchain</h4>
      <p>O sistema dARK registra cada ARK no blockchain, junto com sua URL de destino e metadados essenciais, proporcionando um registro descentralizado e à prova de manipulações de identificadores.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">4</div>
    <div class="step-content">
      <h4>Distribuição de PID</h4>
      <p>Os ARKs recém-criados ou validados podem ser enviados de volta aos repositórios para inclusão em seus registros de metadados, permitindo uma abordagem padronizada para a identificação persistente em toda a rede.</p>
    </div>
  </div>
  
  <div class="workflow-step">
    <div class="step-number">5</div>
    <div class="step-content">
      <h4>Resolução</h4>
      <p>Quando um usuário acessa um ARK, o resolver global redireciona para o resolver dARK, que utiliza o blockchain para recuperar a informação de localização atual, assegurando o acesso persistente mesmo quando as localizações dos recursos mudam.</p>
    </div>
  </div>
</div>

Esta abordagem de integração permite aos agregadores de metadados como LA Referencia melhorar seus serviços com uma infraestrutura de PID descentralizada enquanto preservam os fluxos de trabalho existentes e adicionam valor à rede de repositórios como um todo. Também permite transições sem problemas quando os repositórios movem conteúdo ou mudam de plataforma, já que o sistema de resolução de PID pode ser atualizado sem quebrar links externos.

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
      <li>Transformar este projeto inicial (atualmente trabalhando no IBICT/Brasil) em um serviço regional integral projetado como uma infraestrutura pública, seguindo os princípios estabelecidos pela LA Referencia</li>
      <li>Desenvolver plugins para os sistemas de repositórios e revistas mais utilizados para facilitar a integração perfeita com a infraestrutura dARK</li>
      <li>Implementar persistência descentralizada de metadados para preservar a informação bibliográfica e servir como uma fonte de dados confiável para sistemas analíticos como OpenAlex</li>
    </ul>
    <p>Essas melhorias fortalecerão ainda mais o ecossistema dARK e expandirão sua utilidade dentro do panorama da comunicação acadêmica em toda a América Latina e além.</p>
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





