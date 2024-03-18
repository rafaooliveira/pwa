<template>
<div class="q-ma-xl q-gutter-lg row justify-center">
    <q-input class="col-12" label="E-mail" outlined />
    <q-input class="col-12" label="Senha" outlined type="password" />
    <q-btn
      rounded
      label="Entrar"
      color="primary"
      @click="login()"
    />
</div>
</template>

<script setup>
import { useRouter } from 'vue-router'
const router = useRouter()
function login () {
  try {
    router.push('/home')
  } catch (e) {
    console.log('Erro ao Redirecionar', e)
  }
}
</script>
