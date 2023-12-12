<script setup>
import { onMounted, onUnmounted } from "vue";

//example components
import NavbarDefault from "../..//examples/navbars/NavbarDefault.vue";
import DefaultFooter from "../../examples/footers/FooterDefault.vue";
import Header from "../../examples/Header.vue";

//Vue Material Kit 2 components
import MaterialSocialButton from "@/components/MaterialSocialButton.vue";

// sections
import PresentationCounter from "./Sections/PresentationCounter.vue";
import PresentationExample from "./Sections/PresentationExample.vue";
import data from "./Sections/Data/designBlocksData";
import PresentationInformation from "./Sections/PresentationInformation.vue";

//images
import vueMkHeader from "@/assets/img/header/mitchell-luo.jpg";
import wavesWhite from "@/assets/img/waves-white.svg";
import logoVue from "@/assets/img/logos/vue.jpg";
import logoAngular from "@/assets/img/logos/angular.jpg";
import logoReact from "@/assets/img/logos/react.jpg";

//hooks
const body = document.getElementsByTagName("body")[0];
onMounted(() => {
  body.classList.add("presentation-page");
  body.classList.add("bg-gray-200");
});
onUnmounted(() => {
  body.classList.remove("presentation-page");
  body.classList.remove("bg-gray-200");
});
</script>

<template>
  <div class="container position-sticky z-index-sticky top-0">
    <div class="row">
      <div class="col-12">
        <NavbarDefault :sticky="true" />
      </div>
    </div>
  </div>
  <Header>
    <div
      class="page-header min-vh-75"
      :style="`background-image: url(${vueMkHeader})`"
      loading="lazy"
    >
      <div class="container">
        <div class="row">
          <div class="col-lg-7 text-center mx-auto position-relative">
            <h1
              class="text-white pt-3 mt-n5 me-2"
              :style="{ display: 'inline-block ' }"
            >
              My Portfolio
            </h1>
            <p class="lead text-white px-5 mt-3" :style="{ fontWeight: '500' }">
              รวบรวมผลงาน
            </p>
          </div>
        </div>
      </div>
    </div>
  </Header>

  <div class="card card-body blur shadow-blur mx-3 mx-md-4 mt-n6">
    <PresentationInformation />
    <PresentationCounter />
    <PresentationExample :data="data" />

    <div
      class="container-fluid mt-sm-5 border-radius-xl"
      :style="{
        background: 'linear-gradient(195deg, rgb(66, 66, 74), rgb(25, 25, 25))',
      }"
    >
      <div
        class="page-header py-6 py-md-5 my-sm-3 mb-3 border-radius-xl"
        :style="{
          backgroundImage: `url(${wavesWhite})`,
        }"
        loading="lazy"
      >
        <span class="mask bg-gradient-dark"></span>
        <div class="container">
          <div class="row">
            <div class="d-flex justify-content-center p-5">
              <div class="col-lg-8 ms-lg-5 text-center">
                <h3 class="text-white">เรียน IT ดียังไง</h3>
                <p class="text-white text-md">
                  เรียนรู้การเขียนโปรแกรม การพัฒนาเว็บไซต์ การพัฒนาฐานข้อมูล
                  Machine Learning , AI และ เครื่องมือที่ใช้ในการพัฒนามากมาย
                  รวมไปถึงกระแสในการเปลี่ยนแปลงโลกที่จะเกิดขึ้นในอนาคตข้างหน้า
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="container">
      <div class="row">
        <div class="d-flex flex-column w-100 text-center p-5 mb-8">
          <h3>สิ่งที่สนใจ</h3>
          <div class="d-flex justify-content-center mt-3 flex-wrap">
            <a
              href="https://www.creative-tim.com/product/vue-material-kit-pro"
              class="mx-3"
              data-bs-toggle="tooltip"
              data-bs-placement="bottom"
              title="Vue.js - Is a Progressive JavaScript Framework"
            >
              <img
                :src="logoVue"
                alt="title"
                loading="lazy"
                :style="{ height: '90px' }"
              />
            </a>
            <a
              href="https://www.creative-tim.com/product/vue-material-kit-pro"
              class="mx-3"
              data-bs-toggle="tooltip"
              data-bs-placement="bottom"
              title="Vue.js - Is a Progressive JavaScript Framework"
            >
              <img
                :src="logoAngular"
                alt="title"
                loading="lazy"
                :style="{ height: '90px' }"
              />
            </a>
            <a
              href="https://www.creative-tim.com/product/vue-material-kit-pro"
              class="mx-3"
              data-bs-toggle="tooltip"
              data-bs-placement="bottom"
              title="Vue.js - Is a Progressive JavaScript Framework"
            >
              <img
                :src="logoReact"
                alt="title"
                loading="lazy"
                :style="{ height: '90px' }"
              />
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="py-5">
      <div class="container">
        <div class="row">
          <div class="col-lg-5 ms-auto">
            <h4 class="mb-1">ช่องทางการติดต่อ</h4>
          </div>
          <div class="col-lg-5 me-lg-auto my-lg-auto text-lg-end mt-5">
            <MaterialSocialButton
              route="https://www.facebook.com/saharat.suwannapapond.7"
              component="facebook-square"
              color="facebook"
              label="FB"
            />
            <MaterialSocialButton
              route="https://www.instagram.com/sr_sarus/"
              component="instagram"
              color="instagram"
              label="IG"
            />
          </div>
        </div>
      </div>
    </div>
    <div class="py-5">
      <div class="container">
        <div class="row">
          <div class="col-lg-4 ms-auto">
            <h4 class="mb-1">ที่อยู่</h4>
            <ul style="list-style: none">
              <li>
                <i class="fas fa-map-marker-alt"></i>
                : 86 ม.6 ต.นิคมพัฒนา อ.มะนัง จ.สตูล 91130
              </li>
              <li>
                <i class="fas fa-envelope"></i>
                : saharat.rus@gmail.com
              </li>
              <li>
                <i class="fas fa-phone"></i>
                : 086-9728283
              </li>
            </ul>
          </div>
          <div class="col-lg-6 ms-auto">
            <h4 class="mb-1">แผนที่</h4>
            <iframe
                src="https://www.google.com/maps/embed?pb=!1m24!1m12!1m3!1d3960.4660914156657!2d99.880845725818!3d6.954216768006583!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!4m9!3e6!4m3!3m2!1d6.9541907!2d99.8838718!4m3!3m2!1d6.9541667!2d99.88386109999999!5e0!3m2!1sth!2sth!4v1702349177862!5m2!1sth!2sth" width="100%" height="350" allowFullScreen="" loading="lazy" title="Google Map"></iframe>
          </div>
        </div>
      </div>
    </div>
  </div>
  <DefaultFooter />
</template>
