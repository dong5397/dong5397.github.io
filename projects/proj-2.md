---
layout: post
title: ""
---

<style>
  body {
    font-family: 'Roboto', sans-serif;
    background-color: #f4f4f9;
    margin: 0;
    padding: 0;
    color: #333;
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 20px;
  }

  h1 {
    text-align: center;
    color: #333;
    margin-bottom: 50px;
    font-size: 2.5em;
    position: relative;
  }

  h1::after {
    content: '';
    width: 100px;
    height: 3px;
    background: linear-gradient(135deg, #6e8efb, #a777e3);
    display: block;
    margin: 10px auto 0;
    border-radius: 5px;
  }

  .projects-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
  }

  .project-card {
    background: #fff;
    border-radius: 15px;
    box-shadow: 0 6px 20px rgba(0, 0, 0, 0.1);
    overflow: hidden;
    max-width: 350px;
    text-align: center;
    transition: transform 0.3s, box-shadow 0.3s;
    position: relative;
  }

  .project-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 12px 24px rgba(0, 0, 0, 0.2);
  }

  .project-image {
    width: 100%;
    height: 200px;
    object-fit: cover;
    transition: transform 0.3s;
  }

  .project-card:hover .project-image {
    transform: scale(1.1);
  }

  .project-details {
    padding: 20px;
    position: relative;
    z-index: 2;
  }

  .project-title {
    font-size: 1.75em;
    color: black;
    margin: 0;
    position: relative;
    z-index: 2;
  }

  .project-description {
    font-size: 1em;
    color: #666;
    margin: 10px 0;
    position: relative;
    z-index: 2;
  }

  .project-technologies {
    font-size: 0.9em;
    color: #999;
    margin: 10px 0;
    position: relative;
    z-index: 2;
  }

  .project-link {
    background: linear-gradient(135deg, #6e8efb, #a777e3);
    border-radius: 5px;
    color: #fff;
    display: inline-block;
    margin: 15px 0;
    padding: 10px 20px;
    text-decoration: none;
    transition: background 0.3s;
    position: relative;
    z-index: 2;
  }

  .project-link:hover {
   background: linear-gradient(135deg, #6e8efb, #a777e3);
  }

  .project-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(to bottom, rgba(0, 0, 0, 0.3), transparent 50%);
    border-radius: 15px;
    opacity: 0;
    transition: opacity 0.3s;
  }

  .project-card:hover::before {
    opacity: 1;
  }
</style>

<div class="container">
  <h1>My GitHub Projects</h1>

  <div class="projects-container">
    <div class="project-card">
      <img class="project-image" src="../assets/img/projects/proj-2/main2.png" alt="Awesome App Screenshot">
      <div class="project-details">
        <h2 class="project-title">맛집 사이트</h2>
        <p class="project-description">사용자가 원하는 입맛의 식당을 검색 및 찾아 볼 수 있다.</p>
        <p class="project-technologies">사용기술: React, Node.js, Postgre</p>
        <a class="project-link" href="https://github.com/dong5397/TesteMarketer-app">View Repository</a>
      </div>
    </div>
    <div class="project-card">
      <img class="project-image" src="../assets/img/projects/proj-2/main3.png" alt="Cool Tool Screenshot">
      <div class="project-details">
        <h2 class="project-title">TikTok</h2>
        <p class="project-description">틱톡 AR필터 모집 공고 제작</p>
        <p class="project-technologies">사용기술: React, Node.js, Postgre</p>
        <a class="project-link" href="https://github.com/dong5397/TicTok5397">View Repository</a>
      </div>
    </div>
  </div>
</div>

---
