너는 반응형 디자인과 링크 미리보기와 사용성을 중시하는 프론트엔드 개발자야, html, css, bootstrap을 바탕으로 (추가적인 js와 인라인 스타일은 없이), flex와 container를 사용하여 모바일에서도 사용이 가능한, 카드/캐러셀/모달 컴포넌트를 포함한, #FFDFDE와 #6A7BA2를 컨셉 색깔로 하는, 중고거래 게시판 페이지를 만들어줘. cdn을 사용할 예정이고, index.html에 별도 style.css 없이 해주고, og 태그와 favicon을 만들 예정이므로 주석으로 해당 위치를 추가해줘. webfont도 추가 예정이므로 해당 위치를 주석으로 표시해줘.

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta property="og:title" content="중고 거래 게시판" />
    <meta
      property="og:description"
      content="여러 사람들이 자유롭게 물건을 거래하는 게시판입니다."
    />
    <meta property="og:image" content="image_url.jpg" />
    <meta property="og:url" content="https://example.com" />
    <meta name="twitter:card" content="summary_large_image" />

    <!-- 웹폰트 추가 위치 -->
    <link
      href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@400;700&display=swap"
      rel="stylesheet"
    />

    <!-- Favicon 추가 위치 -->
    <link rel="icon" href="favicon.ico" type="image/x-icon" />

    <!-- Bootstrap CDN -->
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css"
      rel="stylesheet"
    />

    <title>중고 거래 게시판</title>

    <style>
      body {
        font-family: "Noto Sans KR", sans-serif;
        background-color: #ffdfde;
      }

      .header {
        background-color: #6a7ba2;
        color: white;
        padding: 20px;
        text-align: center;
      }

      .card {
        border: none;
        border-radius: 8px;
        margin: 10px 0;
      }

      .card-header {
        background-color: #6a7ba2;
        color: white;
        font-size: 1.25rem;
      }

      .card-body {
        background-color: #fff;
      }

      .carousel-item img {
        max-height: 400px;
        object-fit: cover;
        width: 100%;
      }

      .modal-content {
        background-color: #ffdfde;
      }

      .modal-header {
        background-color: #6a7ba2;
        color: white;
      }

      .footer {
        background-color: #6a7ba2;
        color: white;
        padding: 10px 0;
        text-align: center;
      }
    </style>
  </head>

  <body>
    <!-- Header Section -->
    <div class="header">
      <h1>중고 거래 게시판</h1>
      <p>다양한 물건들을 거래하세요!</p>
    </div>

    <!-- Main Content Section -->
    <div class="container mt-5">
      <!-- Cards for Listings -->
      <div class="row">
        <div class="col-md-4 mb-4">
          <div class="card">
            <div class="card-header">중고 노트북</div>
            <div class="card-body">
              <p>가격: 300,000원</p>
              <p>상태: 양호</p>
              <button
                class="btn btn-primary"
                data-bs-toggle="modal"
                data-bs-target="#modal1"
              >
                상세보기
              </button>
            </div>
          </div>
        </div>
        <div class="col-md-4 mb-4">
          <div class="card">
            <div class="card-header">중고 스마트폰</div>
            <div class="card-body">
              <p>가격: 150,000원</p>
              <p>상태: 사용감 있음</p>
              <button
                class="btn btn-primary"
                data-bs-toggle="modal"
                data-bs-target="#modal2"
              >
                상세보기
              </button>
            </div>
          </div>
        </div>
        <div class="col-md-4 mb-4">
          <div class="card">
            <div class="card-header">중고 자전거</div>
            <div class="card-body">
              <p>가격: 100,000원</p>
              <p>상태: 양호</p>
              <button
                class="btn btn-primary"
                data-bs-toggle="modal"
                data-bs-target="#modal3"
              >
                상세보기
              </button>
            </div>
          </div>
        </div>
      </div>

      <!-- Carousel -->
      <div
        id="carouselExampleIndicators"
        class="carousel slide"
        data-bs-ride="carousel"
      >
        <div class="carousel-indicators">
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="0"
            class="active"
            aria-current="true"
            aria-label="Slide 1"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="1"
            aria-label="Slide 2"
          ></button>
          <button
            type="button"
            data-bs-target="#carouselExampleIndicators"
            data-bs-slide-to="2"
            aria-label="Slide 3"
          ></button>
        </div>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="carousel1.jpg" class="d-block w-100" alt="..." />
          </div>
          <div class="carousel-item">
            <img src="carousel2.jpg" class="d-block w-100" alt="..." />
          </div>
          <div class="carousel-item">
            <img src="carousel3.jpg" class="d-block w-100" alt="..." />
          </div>
        </div>
        <button
          class="carousel-control-prev"
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide="prev"
        >
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button
          class="carousel-control-next"
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide="next"
        >
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>

      <!-- Modals -->
      <div
        class="modal fade"
        id="modal1"
        tabindex="-1"
        aria-labelledby="modalLabel1"
        aria-hidden="true"
      >
        <div class="modal-dialog">
          <div class="modal-content">
            <div class="modal-header">
              <h5 class="modal-title" id="modalLabel1">중고 노트북 상세</h5>
              <button
                type="button"
                class="btn-close"
                data-bs-dismiss="modal"
                aria-label="Close"
              ></button>
            </div>
            <div class="modal-body">
              <p>상태: 사용감 있음</p>
              <p>세부 정보: RAM 8GB, SSD 512GB</p>
            </div>
            <div class="modal-footer">
              <button
                type="button"
                class="btn btn-secondary"
                data-bs-dismiss="modal"
              >
                닫기
              </button>
            </div>
          </div>
        </div>
      </div>

      <div
        class="modal fade"
        id="modal2"
        tabindex="-1"
        aria-labelledby="modalLabel2"
        aria-hidden="true"
      >
        <div class="modal-dialog">
          <div class="modal-content">
            <div class="modal-header">
              <h5 class="modal-title" id="modalLabel2">중고 스마트폰 상세</h5>
              <button
                type="button"
                class="btn-close"
                data-bs-dismiss="modal"
                aria-label="Close"
              ></button>
            </div>
            <div class="modal-body">
              <p>상태: 화면 깨짐</p>
              <p>세부 정보: 64GB 모델, A급 상태</p>
            </div>
            <div class="modal-footer">
              <button
                type="button"
                class="btn btn-secondary"
                data-bs-dismiss="modal"
              >
                닫기
              </button>
            </div>
          </div>
        </div>
      </div>

      <div
        class="modal fade"
        id="modal3"
        tabindex="-1"
        aria-labelledby="modalLabel3"
        aria-hidden="true"
      >
        <div class="modal-dialog">
          <div class="modal-content">
            <div class="modal-header">
              <h5 class="modal-title" id="modalLabel3">중고 자전거 상세</h5>
              <button
                type="button"
                class="btn-close"
                data-bs-dismiss="modal"
                aria-label="Close"
              ></button>
            </div>
            <div class="modal-body">
              <p>상태: 타이어 교체 필요</p>
              <p>세부 정보: 21단 기어, 남성용</p>
            </div>
            <div class="modal-footer">
              <button
                type="button"
                class="btn btn-secondary"
                data-bs-dismiss="modal"
              >
                닫기
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Footer Section -->
    <div class="footer">
      <p>© 2025 중고 거래 게시판</p>
    </div>

    <!-- Bootstrap JS CDN -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
  </body>
</html>
```
