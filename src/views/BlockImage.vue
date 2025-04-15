<!--
 * @Author: Lao Qiao
 * @Date: 2025-04-15 23:22:11
 * @LastEditTime: 2025-04-15 23:27:25
 * @LastEditors: Lao Qiao
 * @FilePath: /Sanyue-ImgHub/src/views/BlockImage.vue
 * 我秃了，但我更强了~
-->
<template>
  <div class="blocked-image-page">
    <div>
      <div>
        抱歉，当前图片已被禁止访问。
        <br />
        Sorry, current image is prohibited from being accessed.
      </div>
      <br />
      <div>
        <span>
          <a href="https://www.missz.me" style="color: cornflowerblue">
            missz
          </a>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
import { useHead } from '@vueuse/head';

export default {
  name: 'BlockedImage',
  setup() {
    useHead({
      title: 'Blocked Image',
      meta: [
        { name: 'robots', content: 'noindex, nofollow' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        { charset: 'UTF-8' },
      ],
    });
  },
};
</script>

<style scoped>
.blocked-image-page {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #f5f5f5;
}
</style>
