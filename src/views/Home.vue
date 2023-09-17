<template>
  <div>
    <bounce-loader :loading="isLoading" :color="'#68d391'" size="100" />
    <px-assets-table-vue v-if="!isLoading" :assets="assets" />
  </div>
</template>

<script>
import PxAssetsTableVue from '@/components/PxAssetsTable.vue'
import { getAssets } from '@/api.js'

export default {
  name: 'HomeView',
  components: {
    PxAssetsTableVue,
  },

  data() {
    return {
      assets: [],
      isLoading: false,
    }
  },

  created() {
    this.getData()
    this.isLoading = true
  },

  methods: {
    async getData() {
      try {
        this.assets = await getAssets()
      } catch (error) {
        console.error(error)
      } finally {
        this.isLoading = false
      }
    },
  },
}
</script>
