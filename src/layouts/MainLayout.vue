<template>
  <div class="q-pa-md">
    <q-layout view="lHh Lpr lff">

        <q-toolbar>
          <q-toolbar-title>
      </q-toolbar-title>

        </q-toolbar>
      

      <q-drawer
      v-if="false"
        v-model="drawer"
        show-if-above
        :width="200"
        :breakpoint="400"
      >
        <q-scroll-area style="height: calc(100% - 150px); margin-top: 150px; border-right: 1px solid rgb(244, 243, 245)">
          <q-list padding>

            <q-item clickable v-ripple to="/" active-class="my-menu-link" exact>
              <q-item-section avatar>
                <q-icon name="ti-home" />
              </q-item-section>

              <q-item-section>
                Inicio
              </q-item-section>
            </q-item>

            <q-item clickable v-ripple to="/paciente" active-class="my-menu-link">
              <q-item-section avatar>
                <q-icon name="ti-user" />
              </q-item-section>
              <q-item-section>
               Paciente
              </q-item-section>
            </q-item>
            <q-item clickable v-ripple to="/funcionario" active-class="my-menu-link">
              <q-item-section avatar>
                <q-icon name="ti-user" />
              </q-item-section>
              <q-item-section>
                Funcionario
              </q-item-section>
            </q-item>

            <q-item clickable v-ripple to="/gestao" active-class="my-menu-link">
              <q-item-section avatar>
                <q-icon name="ti-settings" />
              </q-item-section>
              <q-item-section>
                Gestao
              </q-item-section>
            </q-item>




          </q-list>
        </q-scroll-area>
        <q-img class="absolute-top" src="icons\Crianças.jpg" style="height: 150px">
          <div class="absolute-bottom bg-blue-7">
            <q-avatar size="100px" class="q-mb-sm">
              <img src="icons\Crianças.jpg">
            </q-avatar>
            <div class="text-weight-bold">Bem-vindo</div>

          </div>
        </q-img>

      </q-drawer>

      <q-page-container>
        <router-view></router-view>
      </q-page-container>
    </q-layout>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    const drawer = ref(false)
    return {
      drawer
    }
  }
}
</script>
<style lang="scss">

.my-menu-link{
  color: rgb(238, 238, 238);
  background: amber-5;
}

</style>
