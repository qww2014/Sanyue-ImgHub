<!--
 * @Author: Lao Qiao
 * @Date: 2025-04-15 23:22:11
 * @LastEditTime: 2025-04-15 23:28:07
 * @LastEditors: Lao Qiao
 * @FilePath: /Sanyue-ImgHub/src/views/WhiteListOn.vue
 * 我秃了，但我更强了~
-->
<template>
  <div class="blocked-image-page">
    <div>
      <div>
        抱歉，当前已开启白名单模式，上传的图片需要审核通过后才能展示，请等待审核通过后再进行访问。
        <br />
        Sorry, the whitelist mode is currently enabled, the uploaded images need
        to be audited before they can be displayed, please wait for the audit to
        be passed before visiting.
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
      title: 'White List On',
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
