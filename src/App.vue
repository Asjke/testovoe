<template>
  <div>
    <header class="header">
      <div class="header__container">
        <nav class="header__nav">
          <div class="header__logo">
            <img src="@/assets/logo.svg" alt="Logo">
          </div>
          <div class="header__burger-button">
            <div class="burger">
              <span></span>
              <span></span>
              <span></span>
            </div>
          </div>
        </nav>
      </div>
    </header>

    <main class="main main__container">
      <h1 class="main__title main__title--mobile">Центральная россия — <span class="red">1/3 экономики страны</span></h1>
      <h1 class="main__title main__title--desktop"><span class="red">Центральная россия —</span> 1/3 экономики страны</h1>
      <section>
        <ul class="section__list">
          <li class="section__item">
            <h3 class="section__title">Деньги</h3>
            <ul class="section__sublist">
              <li class="section__subitem">
                <p class="section__subitem-percent">73%</p>
                <p class="section__subitem-title">финансовых влияний</p>
              </li>
              <li class="section__subitem">
                <p class="section__subitem-percent">53%</p>
                <p class="section__subitem-title">накопленных прямых иностранных инвестиций</p>
              </li>
              <li class="section__subitem">
                <p class="section__subitem-percent">29%</p>
                <p class="section__subitem-title">инвестиций в основной капитал</p>
              </li>
            </ul>
          </li>
          <li class="section__item">
            <h3 class="section__title">Производство</h3>
            <ul class="section__sublist">
              <li class="section__subitem">
                <p class="section__subitem-percent">73%</p>
                <p class="section__subitem-title">финансовых влияний</p>
              </li>
              <li class="section__subitem">
                <p class="section__subitem-percent">53%</p>
                <p class="section__subitem-title">накопленных прямых иностранных инвестиций</p>
              </li>
              <li class="section__subitem">
                <p class="section__subitem-percent">29%</p>
                <p class="section__subitem-title">инвестиций в основной капитал</p>
              </li>
            </ul>
          </li>
          <li class="section__item">
            <h3 class="section__title">Рынок</h3>
            <ul class="section__sublist">
              <li class="section__subitem">
                <p class="section__subitem-percent">73%</p>
                <p class="section__subitem-title">финансовых влияний</p>
              </li>
              <li class="section__subitem">
                <p class="section__subitem-percent">53%</p>
                <p class="section__subitem-title">накопленных прямых иностранных инвестиций</p>
              </li>
            </ul>
          </li>
        </ul>
      </section>
      <section>
        <div class="main__map-container">
          <img src="@/assets/map.svg" alt="Logo">
        </div>
      </section>
      <section>
        <div class="main__statistic-container">
          <table>
            <caption>Рост за 2019 год</caption>
            <thead>
            <tr>
              <th></th>
              <th>Центральная Россия</th>
              <th>Российская Федерация</th>
            </tr>
            </thead>
            <tbody>
            <tr>
              <th>Внешняя торговля</th>
              <td>5%</td>
              <td>40%</td>
            </tr>
            <tr>
              <th>Инвестиции</th>
              <td>5%</td>
              <td>40%</td>
            </tr>
            <tr>
              <th>Промышленность</th>
              <td>5%</td>
              <td>40%</td>
            </tr>
            <tr>
              <th>Розничная торговля</th>
              <td>5%</td>
              <td>40%</td>
            </tr>
            <tr>
              <th>Сельское хозяйство</th>
              <td>5%</td>
              <td>40%</td>
            </tr>
            </tbody>
          </table>


        </div>
      </section>
    </main>
    <footer>
      <!-- здесь можно добавить информацию о копирайте, ссылки на социальные сети и т.д. -->
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  mounted() {
    this.$nextTick(function() {
      document.querySelector('.burger').addEventListener('click', function() {
        this.classList.toggle('active');
      });
    })
  }
};
</script>

<style lang="scss" scoped>

.header{
  box-shadow: 0px 4px 8px 0px rgba(9, 30, 66, 0.25), 0px 0px 1px 0px rgba(9, 30, 66, 0.31);
}
.header__container{
  margin: 0 auto;
  max-width: 1194px;

}
.header__nav{
  min-height: 56px;
  padding: 0 32px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  align-content: center;
}
.burger {
  width: 35px;
  height: 30px;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  cursor: pointer;
  border-radius: 5px;
  padding: 3px;
}

.burger span {
  width: 100%;
  height: 2px;
  background: rgba(102, 113, 133, 1); /* меняйте на ваш цвет полосок */
  transition: all 0.3s;
}

.burger.active span:nth-child(1) {
  transform: rotate(-45deg) translate(-4px, 6px);
}

.burger.active span:nth-child(2) {
  opacity: 0;
}

.burger.active span:nth-child(3) {
  transform: rotate(45deg) translate(-4px, -8px);
}
.main{
  max-width: 1194px;
  padding: 0 32px;
}
.main__container{
  margin: 0 auto;
  padding-top: 32px;
}
.red {
  color: rgba(156, 20, 33, 1);
}
.main__title {
  &--mobile {
    font-size: 28px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;

    @media (min-width: 768px) {
      display: none;
    }
  }

  &--desktop {
    font-size: 48px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;

    @media (max-width: 767px) {
      display: none;
    }
  }
}

.section__list {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  list-style: none;
  gap: 32px;
}

.section__item {
  margin-bottom: 20px;
}

.section__sublist {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.section__subitem {
  display: flex;
  gap: 8px;
}
.section__title{
  display: inline-block;
  border-bottom: 4px solid rgba(156, 20, 33, 1);
  margin-bottom: 12px;
}
/* Десктопная версия */
@media (min-width: 768px) {
  .section__list {
    flex-direction: row;
    justify-content: space-between;
  }
}
.section__subitem-percent{
  font-size: 18px;
  font-style: normal;
  font-weight: 700;
  line-height: 24px;
}
.section__subitem-title{
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}
.main__map-container{
  z-index: 1;
  display: flex;
  justify-content: flex-end;
  position: relative;
  img{
    max-width: 100%;
    position: absolute;
    top: -50px;
  }
  @media (max-width: 767px) {
    justify-content: flex-start;
    img {
      position: absolute;
      top: 20px;
    }
  }
}
.main__statistic-container{
  max-width: 546px;
  background-color: rgba(243, 244, 246, 1);
  @media (max-width: 767px) {
    display: none;
  }
}
</style>
