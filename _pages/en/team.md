---
layout: page
title: Team  
description: Our team members working on the dARK project
language: en  
language_reference: team
published: true  
order: 4
---
<h1 class="team-title">Meet the dARK Team</h1>


<p class="team-intro">
  Our international team brings together experts in blockchain technology, persistent identifiers, and digital repositories from across Latin America. Together, we're building the future of decentralized archival infrastructure.
</p>

<div class="team-grid">
  <div class="team-member">
    <div class="team-member-header">
      <h3>Washington Segundo</h3>
      <span class="team-member-role">General Coordination of Scientific and Technical Information at IBICT</span>
    </div>
    <div class="team-member-org">IBICT, BRAZIL</div>
    <div class="team-member-contact">
      <a href="mailto:washingtonsegundo@ibict.br" class="team-email">washingtonsegundo@ibict.br</a>
    </div>
  </div>

  <div class="team-member">
    <div class="team-member-header">
      <h3>Bianca Amaro</h3>
      <span class="team-member-role">Coordinator CEOIS IBICT Project </span>
    </div>
    <div class="team-member-org">IBICT, BRAZIL</div>
  </div>

  <div class="team-member">
    <div class="team-member-header">
      <h3>Lautaro Matas</h3>
      <span class="team-member-role">dARK Team Coordination and Software Development</span>
    </div>
    <div class="team-member-org">LA Referencia</div>
    <div class="team-member-contact">
      <a href="mailto:lautaro.matas@lareferencia.redclara.net" class="team-email">lautaro.matas@lareferencia.redclara.net</a>
    </div>
  </div>

  <div class="team-member">
    <div class="team-member-header">
      <h3>Thiago Nóbrega</h3>
      <span class="team-member-role">Architecture, Blockchain Development, and Infrastructure</span>
    </div>
    <div class="team-member-org">IBICT, BRAZIL</div>
  </div>

  <div class="team-member">
    <div class="team-member-header">
      <h3>J. Edilson S. Filho</h3>
      <span class="team-member-role">Architecture, Blockchain Development, and Infrastructure</span>
    </div>
    <div class="team-member-org">IBICT, BRAZIL</div>
  </div>

  <div class="team-member">
    <div class="team-member-header">
      <h3>Marcio Gurguel</h3>
      <span class="team-member-role">Java Development – Components, Libraries, and DSpace Plugin</span>
    </div>
    <div class="team-member-org">IBICT, BRAZIL</div>
  </div>

   <div class="team-member">
    <div class="team-member-header">
      <h3>Federico Cetrangolo</h3>
      <span class="team-member-role">Administrative Support SCOSS Pledges</span>
    </div>
    <div class="team-member-org">LA Referencia</div>
  </div>
</div>

<section class="partner-institutions">
  <h2>Partner Institutions</h2>
  
  <div class="institutions-container">
    <div class="institution">
      <h3>IBICT</h3>
      <p class="institution-fullname">Instituto Brasileiro de Informação em Ciência e Tecnologia</p>
      <p class="institution-description">The Brazilian Institute of Information in Science and Technology is a federal public research institution linked to the Ministry of Science, Technology, and Innovation.</p>
      <a href="https://www.gov.br/ibict/pt-br" target="_blank" class="institution-link">www.gov.br/ibict ↗</a>
    </div>

   
  </div>
   <div class="institution">
      <h3>LA Referencia</h3>
      <p class="institution-fullname">Red Latinomericana para la Ciencia Abierta</p>
      <p class="institution-description">LA Referencia is a Latin American network of Open Science. It supports national Open Science strategies in Latin America and Spain.</p>
      <a href="https://www.lareferencia.info/en/" target="_blank" class="institution-link">www.lareferencia.info ↗</a>
    </div>
</section>



<style>
  .team-title {
    text-align: center;
    margin-bottom: 1rem;
    color: #2c3e50;
  }
  
  .team-intro {
    text-align: center;
    max-width: 800px;
    margin: 0 auto 3rem;
    font-size: 1.1rem;
    line-height: 1.6;
    color: #555;
  }
  
  .team-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 2rem;
    margin-bottom: 3rem;
  }
  
  .team-member {
    background-color: #f8f9fa;
    border-radius: 8px;
    padding: 1.5rem;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  .team-member:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.1);
  }
  
  .team-member-header h3 {
    margin: 0;
    color: #2c3e50;
  }
  
  .team-member-role {
    display: block;
    font-size: 0.9rem;
    color: #666;
    margin-top: 0.25rem;
  }
  
  .team-member-org {
    display: inline-block;
    background-color: #3498db;
    color: white;
    font-size: 0.8rem;
    padding: 0.2rem 0.6rem;
    border-radius: 4px;
    margin: 0.8rem 0;
  }
  
  .team-member-contact {
    margin-top: 0.8rem;
  }
  
  .team-email {
    color: #3498db;
    text-decoration: none;
    font-size: 0.9rem;
    display: inline-block;
  }
  
  .team-email:hover {
    text-decoration: underline;
  }
  
  /* Estilos para las instituciones asociadas */
  .partner-institutions {
    margin-top: 4rem;
    padding-top: 2rem;
    border-top: 1px solid #eaeaea;
  }
  
  .partner-institutions h2 {
    text-align: center;
    color: #2c3e50;
    margin-bottom: 2rem;
  }
  
  .institutions-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
    gap: 2rem;
  }
  
  .institution {
    background-color: #f8f9fa;
    border-radius: 8px;
    padding: 1.5rem;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  .institution h3 {
    margin-top: 0;
    color: #2c3e50;
    font-size: 1.3rem;
    margin-bottom: 0.5rem;
  }
  
  .institution-fullname {
    font-weight: bold;
    color: #555;
    font-size: 0.95rem;
    margin-bottom: 1rem;
  }
  
  .institution-description {
    font-size: 0.9rem;
    line-height: 1.6;
    color: #666;
    margin-bottom: 1rem;
  }
  
  .institution-link {
    display: inline-block;
    color: #3498db;
    text-decoration: none;
  }
  
  .institution-link:hover {
    text-decoration: underline;
  }
  
  @media (max-width: 768px) {
    .team-grid, 
    .institutions-container {
      grid-template-columns: 1fr;
    }
  }
</style>