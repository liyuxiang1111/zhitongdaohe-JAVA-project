<template>
  <div class="projects-container">
    <div class="container">
      <div v-if="1" class="row">
        <h2 style="margin-top: 50px;margin-bottom: 30px;font-size: large;text-align: center">推荐项目</h2>
        <div v-for="item in list" :key="item.projectId" class="col-lg-3">
          <router-link :to="{ path: '/project/' + item.projectId }">
            <div class="thumbnail">
              <img :src="require('../../../assets/image/projectImg/' + item.projectImg)" alt="" />
              <div class="caption">
                <h3>{{ item.projectName }}</h3>
                <p>{{ item.createTime }}</p>
              </div>
            </div>
          </router-link>
        </div>
      </div>
      <div v-else>
        <h2 style="color: #b1191a">推荐项目表中没有数据!!!</h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list: [],
      imag: require(`@/assets/image/person_simple.jpg`),
      token: '',
      flag: true
    }
  },
  created() {
    this.token = localStorage.getItem('Authorizatio')
    this.initProject()
  },
  methods: {
    async initProject() {
      await this.$http({
        method: 'GET',
        url: 'index/hot/project',
        headers: {
          Authorization: this.token
        }
      }).then(({ data: res }) => {
        console.log(res.data)
        this.list = res.data
        /* console.log(res.data[0].projectId) */
      })
    }
  }
}
</script>

<style lang="less" scoped></style>
