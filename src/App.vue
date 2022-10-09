<template>
  <div>
    <header class="header">
      <div class="header__top">
        <nav class="navbar navbar-expand-lg navbar-light">
          <div class="container">
            <a class="navbar-brand" href="#">
              <img src="IMG/header__logo.png" alt="" />
            </a>
            <button
              class="navbar-toggler"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#navbarText"
              aria-controls="navbarText"
              aria-expanded="false"
              aria-label="Toggle navigation"
            >
              <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarText">
              <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li class="nav-item">
                  <h1 class="nav-link nav__title" href="#">
                    Доставка пасты <span class="nav__moscow">Москва</span>
                  </h1>
                  <ul class="navbar-nav me-auto mb-2 mb-lg-0 gap-4">
                    <li
                      class="
                        nav-item
                        d-flex
                        align-items-center
                        gap-1
                        nav__about
                      "
                    >
                      <img src="IMG/header_nav_img-1.svg" alt="" />
                      Яндекс еда <span class="header__nav-red"></span> 4.8
                      <img src="IMG/header_nav_img-2.svg" alt="" />
                    </li>
                    <li
                      class="
                        nav-item
                        d-flex
                        align-items-center
                        gap-1
                        nav__about
                      "
                    >
                      Время доставки <span class="header__nav-red"></span> от 31
                      мин
                    </li>
                  </ul>
                </li>
              </ul>

              <ul class="navbar-nav mb-2 mb-lg-0 gap-5 align-items-center">
                <li class="nav-item nav__adress">
                  <a class="nav-link" href="#">Заказать звонок</a>
                </li>
                <li class="nav-item nav__adress">
                  <a class="nav-link" href="#">8 499 391-84-49</a>
                </li>
              </ul>
            </div>
          </div>
        </nav>
      </div>

      <div class="container">
        <div class="row mt-2 align-items-center">
          <div class="col-9 p-0 gap-0 align-items-center">
            <div class="row nav__services">
              <a
                href="#!"
                class="col nav__link"
                v-bind:comments="comments"
                v-for="comment in comments"
                v-bind:key="comment.id"
              >
                {{ comment.title }}
              </a>
            </div>
          </div>
          <div class="col-3">
            <div class="row">
              <div
                class="
                  col-6
                  d-flex
                  justify-content-center
                  align-items-center
                  nav__service-link
                "
              >
                <a href="#!">Войти</a>
              </div>
              <div
                class="
                  col-6
                  d-flex
                  justify-content-center
                  align-items-center
                  nav__service-link
                "
              >
                <a href="#!">Корзина | 1</a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  data() {
    return {
      comments: [
        { id: "1", link: "#!", title: "Пицца" },
        { id: "2", link: "#!", title: "Паста" },
        { id: "3", link: "#!", title: "Супы" },
        { id: "4", link: "#!", title: "Салаты" },
        { id: "5", link: "#!", title: "Напитки" },
        { id: "6", link: "#!", title: "Десерты" },
        { id: "7", link: "#!", title: "Бакалея" },
        { id: "8", link: "#!", title: "Антипасти" },
        { id: "9", link: "#!", title: "Акции" },
        { id: "10", link: "#!", title: "Комбо" },
        { id: "11", link: "#!", title: "Контакты" },
      ],
    };
  },
};
</script>

<style>
:root {
  --nav_text: #231f20;
  --yellow: #f7d22d;
  --card_text: #797979;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Montserrat", sans-serif;
}

a {
  text-decoration: none;
}

ul,
ol {
  list-style: none;
}
.nav__title {
  font-weight: 600;
  font-size: 17px;
  color: var(--nav_text);
}

.navbar-nav:nth-child(1) > .nav-link {
  font-weight: 600;
  font-size: 17px;
  line-height: 21px;
  color: var(--nav_text) !important;
}

.nav__moscow {
  color: var(--yellow);
  padding-left: 10px;
}

.nav__about {
  font-weight: 700;
  font-size: 13px;
  line-height: 16px;
  color: var(--nav_text) !important;
}

.header__nav-red {
  display: inline-block;
  width: 3px;
  height: 3px;
  background-color: #ff2e65;
  border-radius: 50%;
}

.nav__adress:first-child > .nav-link {
  font-size: 14px;
  font-weight: 700;
  padding: 7px 27px;
  color: var(--card_text);
  background-color: #f3f3f7;
  border-radius: 28px;
}

.nav__adress:last-child > .nav-link {
  font-weight: 700;
  font-size: 26px;
  line-height: 32px;
  color: var(--yellow);
}

.nav__services > a {
  font-weight: 600;
  font-size: 15px;
  color: var(--nav_text) !important;
}

.nav__service-link:nth-child(1) > a {
  color: var(--card_text) !important;
  font-weight: 700;
  font-size: 16px;
  /* width: 140px; */
}

.nav__service-link:nth-child(2) > a {
  color: var(--nav_text) !important;
  background-color: var(--yellow);
  padding: 7px 20px;
  border-radius: 8px;
  font-weight: 700;
  font-size: 16px;
}

.nav__link {
  display: block;
  position: relative;
  text-align: center;
}

.nav__link::after {
  content: "";
  display: inline-block;
  width: 100%;
  height: 3px;
  background-color: #111;
  opacity: 0;
  border-radius: 0 0 100px 100px;

  position: absolute;
  top: 100%;
  left: 0;
  transition: all 0.4s ease;
}

.nav__link:hover::after {
  opacity: 1;
}
</style>
