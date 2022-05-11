<template>
    <main>
      <div class="fixed-top">
        <navbar/>
      </div>

      <div class="container text-center" style="margin-top: 9rem;">
        <div>
          <h1>Periode 2020/2021</h1>
        </div>
        <div class="col-md-12">
            <div v-if="loading" class="text-center">
              <img src="~/static/assets/loading.gif" alt="loading..." width="50%">
            </div>
          </div>
        <div class="row justify-content-center">
          <div v-for="hi in his" :key="hi.id">
            <div class="col-md-4 text-center" style="margin-bottom: 2rem;">
              <div class="card" style="width: 18rem;">
                <img :src="hi.foto" width="100%" class="card-img-top" alt="ini foto ...">
                <div class="card-body">
                  <h5 class="card-title">{{ hi.nama }}</h5>
                  <p class="card-text">{{ hi.jabatan }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="row justify-content-center" style="margin-top: 2rem; margin-bottom: 2rem;">
            <div class="btn-group" role="group" aria-label="Basic mixed styles example">
            <button type="button" class="btn btn-primary"><NuxtLink class="a text-white" style="text-decoration: none;" to="/about1">2019/2020</NuxtLink></button>
            <button type="button" class="btn btn-success"><NuxtLink class="a text-white" style="text-decoration: none;" to="/about">2020/2021</NuxtLink></button>
            <button type="button" class="btn btn-warning"><NuxtLink class="a text-white" style="text-decoration: none;" to="/about2">2021/2022</NuxtLink></button>
            </div>
        </div>
      <div>
        <end/>
      </div>
    </main>
</template>

<script>
export default {
      mounted() {
    console.log (this.$supabase)
  },
  data() {
    return {
      his: '',
      loading: true,
    }
  },
  mounted () {
    this.ambildata()
  },
  methods: {
    async ambildata() {
      const { data, error } = await this.$supabase
      .from('struks')
      .select()
      if(data)
      this.his = data
      this.loading = false
      if(error) console.log(error)
    }
  }
}
</script>
