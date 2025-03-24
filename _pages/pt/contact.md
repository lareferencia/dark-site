---
layout: page
title: "Contato"
description: "Entre em contato com a equipe dARK"
language: pt
language_reference: contact
published: true
order: 3
---

<div class="contact-header">
  <h1>Contato</h1>
  <p class="lead-text">Tem perguntas ou quer saber mais sobre o dARK? Adoraríamos ouvir de você.</p>
</div>

<h2 class="custom-heading">Entre em Contato</h2>

<div class="contact-card">
  <div class="contact-card-background"></div>
  <div class="contact-card-content">
    <div class="contact-icon-container">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="#8A3691" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="envelope-icon">
        <rect x="2" y="4" width="20" height="16" rx="2" />
        <path d="M22,5L12,13L2,5" />
        <line x1="2" y1="19" x2="7" y2="14" />
        <line x1="17" y1="14" x2="22" y2="19" />
      </svg>
    </div>
    <h3>Envie-nos um Email</h3>
    <p class="contact-description">Para todas as consultas relacionadas ao projeto dARK, entre em contato conosco em:</p>
    <a href="mailto:lareferencia@lareferencia.redclara.net" class="contact-email-link">
      <span>lareferencia@lareferencia.redclara.net</span>
      <i class="fas fa-arrow-right"></i>
    </a>
  </div>
</div>

<h2 class="custom-heading">Apoiar o dARK como Financiador</h2>

<div class="funding-info">
  <p>O projeto dARK conta com o generoso apoio de organizações comprometidas em construir uma infraestrutura sustentável e descentralizada de identificadores persistentes para a ciência aberta global. Ao se tornar um financiador, você se juntará a uma comunidade de instituições visionárias que ajudam a promover a ciência aberta globalmente.</p>
  
  <h3 class="custom-heading-secondary">Por que Apoiar o dARK?</h3>
  <ul>
    <li>Contribuir para uma infraestrutura crítica de ciência aberta</li>
    <li>Apoiar uma abordagem descentralizada para identificadores persistentes</li>
    <li>Fortalecer a soberania dos dados de pesquisa na América Latina e além</li>
    <li>Ajude a criar um ecossistema científico mais inclusivo e equitativo</li>
  </ul>
  
  <div class="note-container">
    <div class="note-header">
      <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="#8A3691" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
        <circle cx="12" cy="12" r="10"></circle>
        <line x1="12" y1="8" x2="12" y2="12"></line>
        <line x1="12" y1="16" x2="12.01" y2="16"></line>
      </svg>
      <h4>Pronto para Apoiar o dARK?</h4>
    </div>
    <div class="note-content">
      <p>Entre em contato conosco para discutir como sua organização pode contribuir para a construção de uma infraestrutura sustentável de ciência aberta.</p>
      <a href="mailto:lareferencia@lareferencia.redclara.net" class="contact-link">lareferencia@lareferencia.redclara.net</a>
    </div>
  </div>
</div>

<style>
  .contact-header {
    text-align: center;
    margin-bottom: 3rem;
    padding-bottom: 1.5rem;
    border-bottom: 1px solid #eaeaea;
  }
  
  .lead-text {
    font-size: 1.2rem;
    color: #555;
    max-width: 800px;
    margin: 0 auto;
  }
  
  .contact-main {
    display: none;
  }
  
  .contact-icon {
    font-size: 3rem;
    color: #8A3691;
    margin-bottom: 1.5rem;
  }
  
  .contact-link {
    display: inline-block;
    margin-top: 1rem;
    font-size: 1.2rem;
    color: #8A3691;
    font-weight: 500;
  }
  
  .funding-info {
    background-color: #f9f9f9;
    padding: 2rem;
    border-radius: 8px;
    margin: 2rem 0 3rem;
  }
  
  /* Estilos importados de architecture.md - modificados para ser mais pequenos */
  .custom-heading {
    font-size: 1.25rem; /* Reduzido de 1.4rem */
    color: #8A3691;
    position: relative;
    margin-bottom: 1.25rem; /* Reduzido de 1.5rem */
    padding-bottom: 0.4rem; /* Reduzido de 0.5rem */
    font-weight: 600;
    border-bottom: 2px solid #eaeaea;
  }
  
  .custom-heading::after {
    content: "";
    position: absolute;
    bottom: -2px;
    left: 0;
    width: 50px; /* Reduzido de 60px */
    height: 2px;
    background-color: #8A3691;
  }
  
  .custom-heading-secondary {
    font-size: 1.1rem; /* Reduzido de 1.2rem */
    color: #555;
    margin-top: 1.25rem; /* Reduzido de 1.5rem */
    margin-bottom: 0.85rem; /* Reduzido de 1rem */
    font-weight: 500;
  }
  
  /* Note container styling - ajustado para títulos mais pequenos */
  .note-header h4 {
    color: #8A3691;
    margin: 0;
    font-size: 1rem; /* Reduzido de 1.1rem */
    font-weight: 600;
    flex-grow: 1;
  }
  
  /* Redução do tamanho do título principal */
  .contact-header h1 {
    font-size: 1.8rem; /* Tamanho mais pequeno para o título principal */
  }
  
  /* Redução do tamanho de outros títulos h3 */
  .contact-main h3 {
    font-size: 1.15rem;
    margin-bottom: 0.75rem;
  }
  
  /* Note container styling importado de architecture.md */
  .note-container {
    margin: 2.5rem 0;
    background-color: #f8f9fe;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(138, 54, 145, 0.08);
    overflow: hidden;
    width: 100%;
    display: block;
  }
  
  .note-header {
    background-color: rgba(138, 54, 145, 0.07);
    padding: 1rem 1.5rem;
    display: flex;
    align-items: center;
    gap: 0.75rem;
    border-bottom: 1px solid rgba(138, 54, 145, 0.1);
    width: 100%;
    box-sizing: border-box;
  }
  
  .note-header h4 {
    color: #8A3691;
    margin: 0;
    font-size: 1rem; /* Reduzido de 1.1rem */
    font-weight: 600;
    flex-grow: 1;
  }
  
  .note-content {
    padding: 1.25rem 1.5rem;
    width: 100%;
    display: block;
    box-sizing: border-box;
  }
  
  .note-container p:last-child {
    margin-bottom: 0;
  }
  
  /* Estilos melhorados para a seção Entre em Contato */
  .contact-card {
    max-width: 600px;
    margin: 2rem auto 3rem;
    position: relative;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 8px 24px rgba(138, 54, 145, 0.12);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  .contact-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 30px rgba(138, 54, 145, 0.18);
  }
  
  .contact-card-background {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(135deg, #f0f7ff 0%, #f9f0ff 100%);
    opacity: 0.8;
    z-index: 1;
  }
  
  .contact-card-content {
    position: relative;
    z-index: 2;
    padding: 2.5rem;
    text-align: center;
  }
  
  .contact-icon-container {
    width: 80px;
    height: 80px;
    margin: 0 auto 1.5rem;
    background-color: rgba(138, 54, 145, 0.1);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #8A3691;
    border: 2px solid rgba(138, 54, 145, 0.2);
    box-shadow: 0 4px 12px rgba(138, 54, 145, 0.15);
    position: relative;
    overflow: hidden;
  }
  
  .envelope-icon {
    width: 40px;
    height: 40px;
    stroke: #8A3691;
    stroke-width: 1.5px;
    transition: transform 0.3s ease;
  }
  
  .contact-card:hover .envelope-icon {
    transform: scale(1.12);
  }
  
  /* Quitar o estilo Font Awesome anterior */
  .fas.fa-envelope {
    display: none;
  }
  
  .contact-card h3 {
    font-size: 1.4rem;
    color: #444;
    margin-bottom: 1rem;
    font-weight: 600;
  }
  
  .contact-description {
    font-size: 1rem;
    color: #666;
    margin-bottom: 1.5rem;
    line-height: 1.5;
  }
  
  .contact-email-link {
    display: inline-flex;
    align-items: center;
    padding: 0.8rem 1.5rem;
    background-color: white;
    border-radius: 50px;
    color: #8A3691;
    font-weight: 500;
    font-size: 1.05rem;
    box-shadow: 0 3px 10px rgba(138, 54, 145, 0.1);
    transition: all 0.2s ease;
    text-decoration: none;
    border: 1px solid rgba(138, 54, 145, 0.2);
  }
  
  .contact-email-link:hover {
    background-color: #8A3691;
    color: white;
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(138, 54, 145, 0.25);
    text-decoration: none;
  }
  
  .contact-email-link i {
    margin-left: 0.8rem;
    font-size: 0.9rem;
    transition: transform 0.2s ease;
  }
  
  .contact-email-link:hover i {
    transform: translateX(3px);
  }
</style>
