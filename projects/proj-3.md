---
layout: default
title: ""
---

<style>
  body {
    font-family: 'Arial', sans-serif;
    line-height: 1.6;
    background-color: #f0f2f5;
    color: #333;
    margin: 0;
    padding: 0;
  }

  .container {
    max-width: 800px;
    margin: 50px auto;
    padding: 20px;
    background-color: #fff;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    animation: fadeIn 1s ease-in-out;
  }

  @keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
  }

  h1, h2 {
    color: #663399; /* 보라색 */
    text-align: center;
  }

  h1 {
    font-size: 2.5em;
    margin-bottom: 20px;
    position: relative;
  }

  h1::after {
    content: '';
    width: 100px;
    height: 3px;
    background: #ffd700; /* 금색 */
    display: block;
    margin: 10px auto 0;
    border-radius: 5px;
  }

  h2 {
    font-size: 1.75em;
    margin-top: 40px;
    margin-bottom: 20px;
    position: relative;
  }

  h2::after {
    content: '';
    width: 50px;
    height: 3px;
    background: #ffd700; /* 금색 */
    display: block;
    margin: 10px auto 0;
    border-radius: 5px;
  }

  p {
    text-align: justify;
    margin-bottom: 20px;
  }

  ul {
    list-style: none;
    padding: 0;
  }

  li {
    background: #f9f9f9;
    margin: 10px 0;
    padding: 15px;
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    transition: transform 0.3s;
  }

  li:hover {
    transform: translateY(-5px);
  }

  .contact-info p {
    margin: 10px 0;
    padding: 10px;
    background: #f9f9f9;
    border-left: 5px solid #663399;
    border-radius: 5px;
  }

  .contact-info a {
    color: #663399;
    text-decoration: none;
    transition: color 0.3s;
  }

  .contact-info a:hover {
    color: #ffd700; /* 금색 */
    text-decoration: underline;
  }

  .footer {
    text-align: center;
    margin-top: 20px;
    font-size: 0.9em;
    color: #666;
  }
</style>

<div class="container">
  <h1>인사말</h1>
  <p>안녕하세요! 저희 웹사이트를 방문해 주셔서 감사합니다. 저희는 최고의 서비스를 제공하기 위해 항상 노력하고 있습니다. 언제든지 문의 사항이나 도움이 필요하시면 연락 주시기 바랍니다.</p>

  <h2>대학생활</h2>
  <ul>
    <li><strong>2019년</strong>: 학교 입학</li>
    <li><strong>2020년</strong>: 2학년, 코로나</li>
    <li><strong>2021~22년</strong>: 군대 입대</li>
    <li><strong>2023년</strong>: 복학</li>
    <li><strong>2024년</strong>: 4학년 시작</li>
  </ul>

  <h2>조직도</h2>
  <ul>
    <li><strong>대학생</strong>: 김동욱</li>
    
  </ul>

  <h2>연락처</h2>
  <div class="contact-info">
  <p><strong>이름</strong>: 김동욱</p>
    <p><strong>전화번호</strong>: 010-2848-5397</p>
    <p><strong>이메일</strong>: <a href="mailto:ehddnr5397@naver.com">ehddnr5397@naver.com</a></p>
  </div>

  <p>저희와 함께 더 나은 미래를 만들어 갑시다. 언제든지 연락 주시면 친절히 응대하겠습니다.</p>

  <div class="footer">
    &copy; 2024 해외여행 추천 사이트
  </div>
</div>
