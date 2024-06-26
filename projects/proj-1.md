---
layout: default
title: "Project One"
---

<section>
  <div class="post-container">
    <h2 class="project-title">소개</h2>
    <div class="project-load">
      <div>
        여행을 계획하고 있지만 어디로 갈지 고민 중이신가요? 저희 사이트는
        여러분의 취향과 선호도를 반영한 맞춤형 여행지를 추천해드립니다.
        <div>
        저희의 주요 기능은 설문조사를 통한 개인 맞춤형 여행지 추천과
        여행일지 기록입니다.
        <div>지금부터 저희 사이트의 기능들을
        소개해드리겠습니다.
        </div>
        </div>
      </div>

      <hr />

      <h3 id="️-개인-맞춤형-여행지-추천">✈️ 개인 맞춤형 여행지 추천</h3>

      <div>
        저희 사이트의 핵심 기능은 설문조사를 통해 개개인의 취향과 선호도를
        반영한 맞춤형 여행지를 추천해드리는 것입니다.
        <div> 설문조사를 통해
        다음과 같은 과정을 거쳐 여러분에게 최적의 여행지를 추천합니다.
        </div>
      </div>

      <div class="custom-card">
        <div class="card-header">
          <i class="fa fa-globe icon"></i>
          <strong>대륙 선택</strong>
        </div>
        <span>가장 먼저 방문하고 싶은 대륙을 선택합니다.</span>
        <div class="card-header">
          <i class="fa fa-flag icon"></i>
          <strong>나라 선택</strong>
        </div>
        <span>선택한 대륙 내에서 방문하고 싶은 나라를 선택합니다.</span>
        <div class="card-header">
          <i class="fa fa-suitcase icon"></i>
          <strong>여행 종류</strong>
        </div>
        <span>어떤 종류의 여행을 선호하시는지 선택합니다.</span>
        <div class="card-header">
          <i class="fa fa-money icon"></i>
          <strong>예산</strong>
        </div>
        <span>여행 예산을 설정합니다.</span>
        <div class="card-header">
          <i class="fa fa-calendar icon"></i>
          <strong>여행 기간</strong>
        </div>
        <span>여행 기간을 선택합니다.</span>
        <div class="card-header">
          <i class="fa fa-bed icon"></i>
          <strong>숙박 시설</strong>
        </div>
        <span>선호하는 숙박 시설을 선택합니다.</span>
        <div class="card-header">
          <i class="fa fa-users icon"></i>
          <strong>여행 동반자</strong>
        </div>
        <span>누구와 함께 여행하는지 선택합니다.</span>
      </div>

      <p>
        이 모든 정보를 바탕으로 여러분에게 딱 맞는 여행지를
        추천해드립니다.
      </p>

      <hr />

      <h3 id="-여행일지-기록">📓 여행일지 기록</h3>

      <div>
        여행을 다녀온 후에는 여행일지를 기록할 수 있는 기능을 제공합니다.
        <div>
        여행 중 찍은 사진과 경험을 기록하여 나만의 여행 일지를
        작성해보세요.
        </div>
        <div>이렇게 작성된 여행 일지는 나중에 다시 볼 수 있도록
        추억을 간직하고, 다른 여행자들과 공유할 수도 있습니다.</div>
      </div>

      <hr />

      <h3 id="-당신의-여행을-더-특별하게">
        ✨ 당신의 여행을 더 특별하게
      </h3>

      <div>
        저희 사이트는 단순한 여행 추천을 넘어, 개개인의 취향에 맞춘 여행을
        제안하여 더욱 특별하고 기억에 남는 여행을 만들어드립니다.</div> <div>저희와
        함께라면 여행 계획이 훨씬 쉬워지고 즐거워질 것입니다.
      </div>

      <div>
        지금 바로 설문조사를 통해 당신만의 맞춤형 여행지를 찾아보세요.
        </div>
        <div>
        여행일지도 작성하여 잊지 못할 여행의 추억을 간직하세요. 저희와
        함께라면, 당신의 여행은 더욱 특별해질 것입니다.
      </div>

      <hr />

      <div class="image-container">
        <img
          src="{{ site.baseurl }}/assets/img/projects/proj-1/main2.jpg"
          alt="Travel Image 1"
          class="travel-image"
        />
        <img
          src="{{ site.baseurl }}/assets/img/projects/proj-1/main3.jpg"
          alt="Travel Image 2"
          class="travel-image"
        />
      </div>
    </div>

  </div>
</section>

<!-- Navigation Section -->
<nav style="text-align: center; margin-top: 30px;">
  <div style="display: inline-block; padding: 10px 20px; background-color: #9b59b6; border-radius: 25px; box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2); transition: background 0.3s ease, transform 0.3s ease, box-shadow 0.3s ease;">
    <a href="{{ site.baseurl }}/survey" style="text-decoration: none; color: #fff; font-size: 20px; font-family: 'Arial', sans-serif; transition: color 0.3s ease;">여행지 알아보기</a>
  </div>
</nav>

<style>
  nav div:hover {
    background-color: #8e44ad;
    transform: scale(1.05);
    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.3);
  }

  nav div a:hover {
    color: #e0e0e0;
  }

  .jua-regular {
    font-family: "Jua", sans-serif;
    font-weight: 400;
    font-style: normal;
  }

  .image-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    margin-top: 20px;
  }

  .travel-image {
    width: 100%;
    height: auto;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  
</style>
