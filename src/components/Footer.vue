<!--
 * @Author: Lao Qiao
 * @Date: 2025-04-15 23:22:11
 * @LastEditTime: 2025-04-15 23:29:49
 * @LastEditors: Lao Qiao
 * @FilePath: /Sanyue-ImgHub/src/components/Footer.vue
 * 我秃了，但我更强了~
-->
<template>
  <div class="page-footer" v-if="!disableFooter">
    <p>
      © 2024-{{ thisYear }}
      <a class="footer-name" href="https://www.missz.me" target="_blank"
        >laoqiao</a
      >
      <a :href="footerLink" target="_blank">
        <font-awesome-icon icon="paper-plane" class="footer-link-icon" />
      </a>
    </p>
  </div>
</template>

<script>
import { mapGetters } from 'vuex';

export default {
  name: 'Footer',
  computed: {
    ...mapGetters(['userConfig']),
    footerLink() {
      return this.userConfig?.footerLink || 'https://www.missz.me';
    },
    thisYear() {
      return new Date().getFullYear();
    },
    disableFooter() {
      return this.userConfig?.disableFooter || false;
    },
  },
};
</script>

<style scoped>
.page-footer {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100vw;
  color: var(--page-footer-text-color);
  font-size: large;
  user-select: none;
}
@media (max-width: 768px) {
  .page-footer {
    font-size: small;
  }
}
.footer-name {
  color: var(--page-footer-name-color);
  font-weight: bold;
  text-decoration: none;
}
.footer-link-icon {
  color: var(--page-footer-name-color);
  margin-left: 5px;
}
</style>
