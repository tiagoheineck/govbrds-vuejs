<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<style>
@import url('https://fonts.cdnfonts.com/css/rawline');
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.11.2/css/all.min.css');
</style>


<template>
  <br-header
  image="https://cdngovbr-ds.estaleiro.serpro.gov.br/design-system/images/logo-positive.png"
  signature="Assinatura da empresa"
  title="Título do Header"
  subtitle="Subtítulo do Header"
  has-menu="true"
  has-search="true"
  placeholder-search="Digite o texto da pesquisa"
  label-search="O que você procura?"
  ><br-header-action
    slot="headerAction"
    has-login=""
    label-login="Entrar"
    image-avatar-login="https://picsum.photos/id/823/400"
    title-links="Acesso Rápido"
    title-functions="Funcionalidades do Sistema"
    list-links="[
    {
      name: 'Link de acesso 1',
      href: '#'
    },
    {
      name: 'Link de acesso 2',
      href: '#'
    },
    {
      name: 'Link de acesso 3',
      href: '#'
    }
  ]"
    list-functions="[
    {
      icon: 'chart-bar',
      name: 'Funcionalidade 1',
      url: '#',
      clickEventName: 'click-funcionalidade-1'
    },
    {
      icon: 'headset',
      name: 'Funcionalidade 2',
      url: '#',
      clickEventName: 'click-funcionalidade-2'
    },
    {
      icon: 'comment',
      name: 'Funcionalidade 3',
      url: '#',
      clickEventName: 'click-funcionalidade-3'
    }
  ]"
    ><br-sign-in
      slot="headerLogin"
      label="Entrar"
      icon="user"
    ></br-sign-in></br-header-action
></br-header>


</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
