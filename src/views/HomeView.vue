<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'
import TheHeader from '@/components/TheHeader.vue'

const isSmallScreen = ref(false)

/*function checkScreen() {
  isSmallScreen.value = window.innerWidth < 1280
}*/

function checkScreen() {
  isSmallScreen.value = window.matchMedia('(max-width: 1279px)').matches
}

onMounted(() => {
  checkScreen()
  window.addEventListener('resize', checkScreen)
})

onUnmounted(() => {
  window.removeEventListener('resize', checkScreen)
})
</script>

<template>
  <div v-if="!isSmallScreen">
    <TheHeader />

    <!--  TODO : Refactor HTML -->
    <main>
      <div class="hero-header" style="padding-inline: 1rem">
        <div>
          <img src="/image%202%2028.png" alt="" />
        </div>
        <div>
          <div><img src="/image.png" alt="" /></div>
          <div>
            <article style="display: flex; flex-flow: column">
              <span>ULTIMATE</span>
              <span>SALE</span>
              <span>NEW COLLECTION</span>
            </article>
            <a href="">
              <div class="btn">SHOP NOW</div>
            </a>
          </div>
          <div>
            <img src="/image2.png" alt="" />
          </div>
        </div>

        <div>
          <img src="/image%20227.png" alt="" />
        </div>
      </div>

      <div class="logos">
        <div>
          <img src="/chanel.png" alt="" />
          <img src="/lvmh.png" alt="" />
          <img src="/prada.png" alt="" />
          <img src="/calvin-klein.png" alt="" />
          <img src="/denim.png" alt="" />
        </div>
      </div>

      <section class="deal-of-the-month">
        <div>
          <div>
            <div class="head">
              <div>
                <h2>Deals Of The Month</h2>
                <p>
                  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Scelerisque duis ultrices
                  sollicitudin aliquam sem. Scelerisque duis ultrices sollicitudin
                </p>
              </div>

              <a href="#">
                <div class="btn">Buy Now</div>
              </a>
            </div>

            <div class="subhead">
              <h3>Hurry, Before It’s Too Late!</h3>

              <div class="timer">
                <div class="item">
                  <div class="time">
                    <span>02</span>
                  </div>
                  <p>Days</p>
                </div>
                <div class="item">
                  <div class="time">
                    <span>06</span>
                  </div>
                  <p>Hr</p>
                </div>
                <div class="item">
                  <div class="time">
                    <span>05</span>
                  </div>
                  <p>Mins</p>
                </div>
                <div class="item">
                  <div class="time">
                    <span>30</span>
                  </div>
                  <p>Sec</p>
                </div>
              </div>
            </div>
          </div>
          <div class="products-section">
            <div class="products">
              <div class="image-slider">
                <img src="/product-slider-1.png" alt="" />

                <div class="promo" style="">
                  <div style="">
                    01
                    <div class="bar"></div>
                    Spring Sale
                  </div>
                  <span>30% OFF</span>
                </div>
              </div>
              <div class="image-slider">
                <img src="/product-slider-2.png" alt="" />
              </div>
              <div class="image-slider">
                <img src="/product-slider-3.png" alt="" />
              </div>
              <div class="button-slider">
                <button></button>
                <button></button>
                <button></button>
                <button></button>
              </div>
            </div>
          </div>
        </div>
      </section>
      <section class="new-arrivals">
        <div>
          <div class="head">
            <h2>New Arrivals</h2>
            <p class="desc">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Scelerisque duis ultrices
              sollicitudin aliquam sem. Scelerisque duis ultrices sollicitudin
            </p>
          </div>

          <div class="categories">
            <div class="category-list">
              <a href="#">
                <div class="category-item">Men’s Fashion</div>
              </a>
              <a href="#">
                <div class="category-item">Women’s Fashion</div>
              </a>
              <a href="#">
                <div class="category-item">Women Accessories</div>
              </a>
              <a href="#">
                <div class="category-item">Men Accessories</div>
              </a>
              <a href="#">
                <div class="category-item">Discount Deals</div>
              </a>
            </div>
          </div>

          <div class="products">
            <div class="product-card">
              <img src="/Images.png" alt="" />
              <div class="product-detail">
                <div class="header-product-detail">
                  <div>
                    <h4 class="title">Shiny Dress</h4>
                    <p class="subtitle">Al Karam</p>
                  </div>
                  <div class="stars">
                    <!-- STARS -->
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                  </div>
                </div>
                <p class="reviews">(4.1k) Customer Reviews</p>
                <div class="product-sale">
                  <p class="price">$95.50</p>
                  <p class="alert">Almost Sold Out</p>
                </div>
              </div>
            </div>
            <div class="product-card">
              <img src="/Images-2.png" alt="" />
              <div class="product-detail">
                <div class="header-product-detail">
                  <div>
                    <h4 class="title">Long Dress</h4>
                    <p class="subtitle">Al Karam</p>
                  </div>
                  <div class="stars">
                    <!-- STARS -->
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                  </div>
                </div>
                <p class="reviews">(4.1k) Customer Reviews</p>
                <div class="product-sale">
                  <p class="price">$95.50</p>
                  <p class="alert">Almost Sold Out</p>
                </div>
              </div>
            </div>
            <div class="product-card">
              <img src="/Images-4.png" alt="" />
              <div class="product-detail">
                <div class="header-product-detail">
                  <div>
                    <h4 class="title">Full Sweater</h4>
                    <p class="subtitle">Al Karam</p>
                  </div>
                  <div class="stars">
                    <!-- STARS -->
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                  </div>
                </div>
                <p class="reviews">(4.1k) Customer Reviews</p>
                <div class="product-sale">
                  <p class="price">$95.50</p>
                  <p class="alert">Almost Sold Out</p>
                </div>
              </div>
            </div>

            <div class="product-card">
              <img src="/Images-1.png" alt="" />
              <div class="product-detail">
                <div class="header-product-detail">
                  <div>
                    <h4 class="title">White Dress</h4>
                    <p class="subtitle">Al Karam</p>
                  </div>
                  <div class="stars">
                    <!-- STARS -->
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                  </div>
                </div>
                <p class="reviews">(4.1k) Customer Reviews</p>
                <div class="product-sale">
                  <p class="price">$95.50</p>
                  <p class="alert">Almost Sold Out</p>
                </div>
              </div>
            </div>
            <div class="product-card">
              <img src="/Images-3.png" alt="" />
              <div class="product-detail">
                <div class="header-product-detail">
                  <div>
                    <h4 class="title">Colorful Dress</h4>
                    <p class="subtitle">Al Karam</p>
                  </div>
                  <div class="stars">
                    <!-- STARS -->
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                  </div>
                </div>
                <p class="reviews">(4.1k) Customer Reviews</p>
                <div class="product-sale">
                  <p class="price">$95.50</p>
                  <p class="alert">Almost Sold Out</p>
                </div>
              </div>
            </div>
            <div class="product-card">
              <img src="/Images-5.png" alt="" />
              <div class="product-detail">
                <div class="header-product-detail">
                  <div>
                    <h4 class="title">White Shirt</h4>
                    <p class="subtitle">Al Karam</p>
                  </div>
                  <div class="stars">
                    <!-- STARS -->
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                    <img src="/stars.svg" alt="" />
                  </div>
                </div>
                <p class="reviews">(4.1k) Customer Reviews</p>
                <div class="product-sale">
                  <p class="price">$95.50</p>
                  <p class="alert">Almost Sold Out</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="view-more">
          <a href="#">
            <div class="btn">View More</div>
          </a>
        </div>
      </section>
    </main>

    <!--    FOOTER -->
    <footer
      style="padding: 1rem; text-align: center; background: black; color: #fff; line-height: 1.5"
    >
      <p>
        Développer par
        <a
          href="https://aymericdelange.fr/"
          target="_blank"
          style="text-decoration: underline; font-weight: 700"
          >Aymeric DE LANGE</a
        >
        -
        <a
          href="https://github.com/AyCoding/fasco-website"
          target="_blank"
          style="text-decoration: underline; font-weight: 700"
          >Code Source</a
        >
      </p>
      <p>
        Une création de
        <a
          href="https://www.figma.com/community/file/1261030123322260154"
          target="_blank"
          style="text-decoration: underline; font-weight: 700"
        >
          Hamza Anza
        </a>
        via Figma Community sous licence
        <a
          href="https://creativecommons.org/licenses/by/4.0/deed.fr"
          target="_blank"
          style="font-weight: 700; text-decoration: underline"
          >CC BY 4.0</a
        >
      </p>
    </footer>
  </div>
  <div
    v-else
    class="disclaimer"
    style="
      text-align: center;
      margin-top: 10rem;
      padding-inline: 1rem;
      line-height: 1.5;
      text-wrap: balance;
    "
  >
    Veuillez utiliser un écran plus grand (au moins 1280 pixels de largeur).
  </div>
</template>
