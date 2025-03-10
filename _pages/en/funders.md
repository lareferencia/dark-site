---
layout: page
title: "Funders"
description: "Organizations supporting the dARK project"
language: en
language_reference: funders
published: true
order: 2
---

<div class="funders-header">
  <h1>Our Financial Supporters</h1>
  <p class="lead-text">The organizations that make dARK possible through their generous support</p>
</div>

## Primary Funders

<div class="funder-card primary">
  <div class="logo-container">
    <img src="{{ site.baseurl }}/assets/img/ibict-logo.png" alt="IBICT Logo" class="funder-logo">
  </div>
  <div class="funder-info">
    <h3>Brazilian Institute of Information in Science and Technology (IBICT)</h3>
       <p>IBICT has been the primary host and funder of the dARK project, providing crucial resources and infrastructure support since its inception. With a long history of driving innovation in scientific communication, IBICT consistently contributes to groundbreaking projects for the Brazilian science ecosystem while maintaining a deep tradition of regional collaboration across Latin America.</p>

    <a href="https://www.gov.br/ibict/pt-br" class="funder-link" target="_blank">Visit website →</a>
  </div>
</div>

## Supporting Organizations

<div class="funder-card">
  <div class="logo-container">
    <img src="{{ site.baseurl }}/assets/img/lareferencia-logo.png" alt="LA Referencia Logo" class="funder-logo">
  </div>
  <div class="funder-info">
    <h3>LA Referencia</h3>
        <p>LA Referencia has been a key strategic partner for the dARK initiative, providing both technical expertise and institutional support. Their collaboration is essential for the future regional expansion of dARK across Latin America and other regions, helping to create a sustainable federated PID infrastructure for the Global Open Science Ecosystem.</p>
    <a href="http://www.lareferencia.info/en/" class="funder-link" target="_blank">Visit website →</a>
  </div>
</div>

<div class="funder-card">
  <div class="logo-container">
    <img src="{{ site.baseurl }}/assets/img/scoss-logo.png" alt="SCOSS Logo" class="funder-logo">
  </div>
  <div class="funder-info">
    <h3>Global Sustainability Coalition for Open Science Services (SCOSS)</h3>
    <p>The backing of SCOSS pledges has been instrumental in securing financial resources for the continued development and sustainability of the dARK project.</p>
    <a href="https://scoss.org/" class="funder-link" target="_blank">Visit website →</a>
  </div>
</div>

## SCOSS Pledgers

<div class="pledgers-section">
  <h3>Organizations that have supported dARK through SCOSS</h3>
  <p class="coming-soon">Complete pledgers list coming soon</p>
  
  <!-- Cuando tengas la lista, reemplaza esto con una grid de logos o lista como esta:
  <div class="pledgers-grid">
    {% for pledger in site.data.pledgers %}
      <div class="logo-container pledger-logo-container">
        <img src="{{ site.baseurl }}/assets/img/pledgers/{{ pledger.logo }}" alt="{{ pledger.name }} Logo" class="pledger-logo">
      </div>
    {% endfor %}
  </div>
  -->
</div>

<div class="support-cta">
  <h2>Interested in Supporting dARK?</h2>
  <p>Join the growing community of organizations helping to build a sustainable, decentralized persistent identifier infrastructure for global open science.</p>
  <a href="{{ site.baseurl }}/en/contact" class="cta-button">Contact Us About Supporting dARK</a>
</div>

<style>
  .funders-header {
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
  
  .funder-card {
    display: flex;
    margin-bottom: 2.5rem;
    padding: 1.5rem;
    border-radius: 8px;
    background-color: #f9f9f9;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
  }
  
  .funder-card.primary {
    background-color: #f0f7ff;
    border-left: 5px solid #8A3691;
  }
  
  .logo-container {
    width: 180px;
    height: 90px;
    margin-right: 1.5rem;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    background-color: white;
    border-radius: 6px;
    padding: 10px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.05);
  }
  
  .funder-logo {
    max-width: 95%;
    max-height: 80px;
    object-fit: contain;
  }
  
  .funder-info {
    flex: 1;
  }
  
  .funder-info h3 {
    margin-top: 0;
    color: #333;
  }
  
  .funder-link {
    display: inline-block;
    margin-top: 0.5rem;
    color: #8A3691;
    font-weight: 500;
  }
  
  .pledgers-section {
    margin: 3rem 0;
    padding: 2rem;
    background-color: #f5f5f5;
    border-radius: 8px;
    text-align: center;
  }
  
  .coming-soon {
    font-style: italic;
    color: #666;
  }
  
  .pledgers-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
    gap: 1.5rem;
    margin-top: 2rem;
  }
  
  .pledger-logo-container {
    margin: 0 auto;
  }
  
  .support-cta {
    margin-top: 4rem;
    padding: 2rem;
    text-align: center;
    background-color: #f9f9f9;
    border-radius: 8px;
    border: 1px solid #eaeaea;
  }
  
  .cta-button {
    display: inline-block;
    margin-top: 1rem;
    padding: 0.8rem 1.5rem;
    background-color: #8A3691;
    color: white;
    text-decoration: none;
    border-radius: 4px;
    font-weight: 500;
    transition: background-color 0.2s;
  }
  
  .cta-button:hover {
    background-color: #8A3691;
    text-decoration: none;
    color: white;
  }
  
  @media (max-width: 768px) {
    .funder-card {
      flex-direction: column;
    }
    
    .logo-container {
      margin: 0 auto 1.5rem auto;
    }
  }
</style>
