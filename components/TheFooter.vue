<template>
  <div>
    <footer class="footer">
      <div class="footer__container container pt-4 pb-4">
        <div class="footer__item d-flex justify-content-between align-items-center">
          <div class="footer__info d-block mb-phone">
            <div class="footer__logo">
              <p class="footer__text-contact dt m-0">Information</p>
            </div>
            <div class="footer__links mt-3 text-left">
              <a href="https://github.com/manucherkm" class="footer__link mb-2" target="_blank">My GitHub</a>
              <a href="https://rapidapi.com/gatzuma/api/deep-translate1/" target="_blank" class="footer__link mb-2">Used
                API</a>

              <a href="https://github.com/ManucherKM/Portfolio-One" class="footer__link mb-2" target="_blank">This
                project is on GitHub</a>
            </div>
          </div>
          <ul class="footer__list mb-phone" v-for="list in massList" :key="list.id">
            <li v-for="item in itemFooterOne" :key="item.id" class="footer__element mb-3">
              <NuxtLink :to="item.link" class="footer__link">{{
                  item.text
              }}</NuxtLink>
            </li>
          </ul>
          <div class="footer__contact text-right">
            <p class="footer__text-contact dt">Contact</p>
            <p class="footer__E-mail">
              <a href="https://www.google.com/intl/ru/gmail/about/" class="footer__link"
                target="_blank">translate@gmail.com</a>
            </p>
            <p class="footer__number">
              <a ref="number" href="#" class="footer__link">+7 (987) 432-32-23</a>
            </p>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
const itemFooterOne = ref([
  { id: Date.now, text: "Home", link: "#" },
  { id: Date.now, text: "About Us", link: "#" },
  { id: Date.now, text: "Contact", link: "#" },
  { id: Date.now, text: "Support", link: "#" },
]);

const massList = ref([{ id: Date.now() }, { id: Date.now() }]);
</script>
