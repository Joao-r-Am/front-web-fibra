<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <q-avatar style="width: 110px">
          <q-img src="src/assets/fibra-logo.png" />
        </q-avatar>
        <q-toolbar-title> Home </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer show-if-above v-model="leftDrawerOpen" side="left" bordered>
      <q-list>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import EssentialLink, {
  EssentialLinkProps,
} from 'src/components/home/EssentialLink.vue';

const essentialLinks: EssentialLinkProps[] = [
  {
    title: 'Parâmetros',
    caption: 'parâmetros de criação',
    icon: 'tune',
    link: 'https://quasar.dev',
  },
  {
    title: 'Tabelas',
    caption: 'tabelas de produtos',
    icon: 'list',
    link: 'https://github.com/quasarframework',
  },
  {
    title: 'Cadastros',
    caption: 'cadastre novas entradas',
    icon: 'app_registration',
    link: 'https://chat.quasar.dev',
  },
  {
    title: 'Embarques',
    caption: 'ultimos embarques',
    icon: 'flight_takeoff',
    link: 'https://forum.quasar.dev',
  },
  {
    title: 'Financeiro',
    caption: 'confira as ultimas atualições',
    icon: 'payments',
    link: 'https://twitter.quasar.dev',
  },
  {
    title: 'Relatório',
    caption: 'relatório de entregas',
    icon: 'lab_profile',
    link: 'https://facebook.quasar.dev',
  },
  {
    title: 'Gerencial',
    caption: 'gerencie e descreva novas opções',
    icon: 'manage_accounts',
    link: 'https://awesome.quasar.dev',
  },
  {
    title: 'Woodbank',
    caption: 'verifique os produtos disponiveis',
    icon: 'forest',
    link: 'https://awesome.quasar.dev',
  },
];

const leftDrawerOpen = ref(false);
</script>
