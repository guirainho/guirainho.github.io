---
layout: default
title: "Home"
---

<style>
  /* Fundo sutil azul-gelo acinzentado */
  body {
    background-color: #f0f4f8 !important;
    color: #1e293b;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  }

  .site-header {
    border-top: 5px solid #0284c7 !important;
    background-color: #ffffff;
  }

  .main-container {
    max-width: 960px;
    margin: 0 auto;
    padding: 48px 20px 80px 20px;
  }

  /* Cabeçalho com visual Tech */
  .hero-section {
    margin-bottom: 48px;
    border-left: 4px solid #0284c7;
    padding-left: 20px;
  }

  .hero-tag {
    display: inline-block;
    font-size: 0.75rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 1.2px;
    color: #0284c7;
    margin-bottom: 8px;
  }

  .hero-title {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    font-size: 2.8rem;
    font-weight: 800;
    line-height: 1.15;
    color: #0f172a;
    margin: 0 0 16px 0;
    letter-spacing: -0.8px;
  }

  .hero-description {
    font-size: 1.1rem;
    line-height: 1.6;
    color: #475569;
    max-width: 620px;
    margin: 0;
  }

  /* Grade de Cards */
  .posts-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 24px;
  }

  /* Card com destaque superior em gradiente azul */
  .card-post {
    position: relative;
    background: #ffffff;
    border-radius: 14px;
    padding: 28px 24px;
    border: 1px solid #e2e8f0;
    box-shadow: 0 4px 12px rgba(15, 23, 42, 0.04);
    text-decoration: none !important;
    display: flex;
    flex-direction: column;
    overflow: hidden;
    transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);
  }

  .card-post::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, #0284c7, #38bdf8);
    opacity: 0;
    transition: opacity 0.25s ease;
  }

  .card-post:hover:not(.disabled) {
    transform: translateY(-5px);
    box-shadow: 0 16px 30px rgba(2, 132, 199, 0.12);
    border-color: #cbd5e1;
  }

  .card-post:hover:not(.disabled)::before {
    opacity: 1;
  }

  /* Badge em azul-cobalto */
  .badge {
    align-self: flex-start;
    background: #0369a1;
    color: #ffffff;
    font-size: 0.7rem;
    font-weight: 700;
    letter-spacing: 1px;
    padding: 5px 12px;
    border-radius: 20px;
    margin-bottom: 16px;
    text-transform: uppercase;
    box-shadow: 0 2px 6px rgba(3, 105, 161, 0.25);
  }

  .card-title {
    font-size: 1.25rem;
    font-weight: 700;
    color: #0f172a;
    margin: 0 0 12px 0;
    line-height: 1.35;
  }

  .card-text {
    font-size: 0.92rem;
    color: #64748b;
    line-height: 1.55;
    margin: 0;
  }

  /* Estilo para Cards futuros */
  .card-post.disabled {
    background: #f8fafc;
    border: 1px dashed #cbd5e1;
    cursor: default;
    box-shadow: none;
  }

  .card-post.disabled::before {
    display: none;
  }

  .card-post.disabled .badge {
    background: #94a3b8;
    box-shadow: none;
  }

  .card-post.disabled .card-title {
    color: #64748b;
  }

  .card-post.disabled .card-text {
    color: #94a3b8;
  }
</style>

<div class="main-container">
  
  <header class="hero-section">
    <span class="hero-tag">Laboratório de Estudos</span>
    <h1 class="hero-title">Posts da disciplina</h1>
    <p class="hero-description">
      Ambiente dedicado a documentar os aprendizados, desafios práticos e reflexões teóricas ao longo do curso de Computação Visual.
    </p>
  </header>

  <section class="posts-grid">

    <!-- Card: Post 1 -->
    <a href="{{ site.baseurl }}{% post_url 2026-08-18-post-1 %}" class="card-post">
      <span class="badge">POST 01</span>
      <h2 class="card-title">Primeiras Impressões</h2>
      <p class="card-text">
        O que eu imaginava encontrar na disciplina e o que comecei a entender sobre a fundamentação exata e algorítmica.
      </p>
    </a>

    <!-- Card: Post 2 -->
    <a href="{{ site.baseurl }}{% post_url 2026-08-18-post-2 %}" class="card-post">
      <span class="badge">POST 02</span>
      <h2 class="card-title">OpenGL e Funcionamento do Olho</h2>
      <p class="card-text">
        Primitivas geométricas na GPU, a anatomia da retina e a ponte entre a visão biológica e digital.
      </p>
    </a>

    <!-- Card: Post 3 (Em breve) -->
    <div class="card-post disabled">
      <span class="badge">POST 03</span>
      <h2 class="card-title">Em breve...</h2>
      <p class="card-text">
        Espaço reservado para a publicação das próximas semanas de aula.
      </p>
    </div>

  </section>
</div>
