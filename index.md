---
layout: default
title: "Home"
---

<style>
  body {
    background-color: #f7f6f2 !important;
    color: #2b303a;
  }

  .main-container {
    max-width: 900px;
    margin: 0 auto;
    padding: 40px 20px 80px 20px;
  }

  .hero-section {
    margin-bottom: 50px;
  }

  .hero-title {
    font-family: "Playfair Display", Georgia, "Times New Roman", serif;
    font-size: 3.2rem;
    font-weight: 700;
    line-height: 1.15;
    color: #0b1d33;
    margin-bottom: 24px;
    letter-spacing: -0.5px;
  }

  .hero-description {
    font-size: 1.15rem;
    line-height: 1.6;
    color: #4a5568;
    max-width: 580px;
    margin: 0;
  }
  
  .posts-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
    gap: 24px;
  }

  .card-post {
    background: #ffffff;
    border-radius: 16px;
    padding: 28px 24px;
    border: 1px solid rgba(0, 0, 0, 0.05);
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.03);
    text-decoration: none !important;
    display: flex;
    flex-direction: column;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .card-post:hover:not(.disabled) {
    transform: translateY(-4px);
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.07);
  }

  .badge {
    align-self: flex-start;
    background-color: #091a2b;
    color: #ffffff;
    font-size: 0.72rem;
    font-weight: 800;
    letter-spacing: 0.8px;
    padding: 5px 10px;
    border-radius: 6px;
    margin-bottom: 18px;
    text-transform: uppercase;
  }

  .card-title {
    font-size: 1.35rem;
    font-weight: 700;
    color: #111827;
    margin: 0 0 14px 0;
    line-height: 1.3;
  }

  .card-text {
    font-size: 0.95rem;
    color: #6b7280;
    line-height: 1.5;
    margin: 0;
  }

  .card-post.disabled {
    background-color: rgba(255, 255, 255, 0.6);
    border: 1px solid rgba(0, 0, 0, 0.03);
    cursor: default;
  }

  .card-post.disabled .badge {
    background-color: #a0aec0;
  }

  .card-post.disabled .card-title {
    color: #718096;
  }

  .card-post.disabled .card-text {
    color: #a0aec0;
  }
</style>

<div class="main-container">
  
  <header class="hero-section">
    <h1 class="hero-title">Posts da disciplina</h1>
    <p class="hero-description">
      Ambiente dedicado a organizar meus posts semanais da disciplina de Computação Visual
    </p>
  </header>

  <section class="posts-grid">

    <!-- Card: Post 1 (Ativo / Com link) -->
    <a href="{{ site.baseurl }}{% post_url 2026-08-18-post-1 %}">
      <span class="badge">POST 01</span>
      <h2 class="card-title">Primeiras Impressões</h2>
      <p class="card-text">
        O que eu imaginava encontrar na disciplina e o que comecei a entender sobre a fundamentação exata e algorítmica.
      </p>
    </a>

    <!-- Card: Post 2 (Ativo) -->
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
