<template>
  <div class="page-error">
    <img src="~assets/images/page-error/collage_404.webp" />
    <div class="page-link">
      <span class="page-span">404</span>
      <h1 class="page-title">Page Not Found</h1>
      <nuxt-link to="" class="btn button">Back to Home Page</nuxt-link>
    </div>
    <div class="page-logo">
      <nuxt-link to="" class="logo-relative">
        <span>
          <img src="~assets/images/page-error/logo_light.svg" />
          <img src="~assets/images/page-error/logo_dark.svg" class="absolute" />
        </span>
        <h4>ShopPoint</h4>
      </nuxt-link>
    </div>
  </div>
</template>
<script>
import { defineComponent } from "@nuxtjs/composition-api";

export default defineComponent({
  layout: "Error",
  setup() {},
});
</script>

<style lang="scss">
.page-error {
  flex: 1;
  padding: 15px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  position: relative;
  height: 100vh;
  overflow: hidden;
  img {
    display: block;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    max-height: calc(100% - 30px);
    max-width: calc(100% - 30px);
    width: auto;
  }
  .page-link {
    position: relative;
    z-index: 2;
    width: 592px;
    height: 592px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    .page-span {
      color: #00193b;
      font-size: 120px;
      line-height: 1.1;
      font-family: "Archivo SemiExpanded", sans-serif;
      font-weight: 700;
    }
    .page-title {
      font-size: 38px;
      color: #00193b;
      font-weight: 700;
    }
    .button {
      background-color: #00ba9d;
      border: 1px solid #01c8a9;
      color: #fff;
      box-shadow: 0 1px 10px rgba(2, 202, 171, 0.35);
      margin: 40px auto 0;
      max-width: 300px;
      width: 100%;
    }
    .btn {
      height: 44px;
      border-radius: 23px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 16px;
      line-height: 1;
      font-size: 16px;
      font-family: "Archivo SemiExpanded", sans-serif;
      font-weight: 600;
      padding: 0 26px;
      transition: 0.3s ease-in-out;
      cursor: pointer;
    }
    ::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      z-index: -1;
      width: 100%;
      height: 100%;
      background: linear-gradient(
        163.23deg,
        rgba(255, 255, 255, 0.0001) 38.07%,
        rgba(240, 240, 240, 0.186708) 87.83%
      );
      box-shadow: 12px 6px 15px rgba(89, 104, 122, 0.190023), inset 2px 2px 2px #ffffff;
      -webkit-backdrop-filter: blur(19.028px);
      backdrop-filter: blur(19.028px);
      border-radius: 50%;
    }
  }
  .page-logo {
    .logo-relative {
      position: relative;
      display: inline-flex;
      align-items: center;
      gap: 12px;
      width: 27px;
      img {
        display: block;
        width: 100%;
        height: auto;
        object-fit: cover;
        max-width: 100%;
      }
      .absolute {
        display: none;
        top: 0px;
        left: 0px;
        position: absolute;
      }
      h4 {
        font-size: 16px;
        margin-left: -3px;
        text-align: center;
        font-weight: bold;
        margin: 20px 30px;
        color: #00193B;
      }
    }
  }
}
</style>
