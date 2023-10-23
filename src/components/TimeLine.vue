<template>
  <main>
    <div class="telaTimeline">
      <Timeline :perfilTimeline="perfilTimeline" :eventosTimeline="listaEventos" />
    </div>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { Timeline } from '@devix-tecnologia/timeline-vue'
import '@devix-tecnologia/timeline-vue/dist/style.css'

export default defineComponent({
  components: { Timeline },
  setup() {
    const perfilTimeline = {
      nome: 'Maria do Socorro',
      imagem: 'https://this-person-does-not-exist.com/img/avatar-gen11071f8e0802a35d66684ee9376722b2.jpg',
      icone: 'person'
    }
    const listaEventos = [
      {
        data: new Date('2023-04-26T18:10Z'),
        previsto: new Date('2023-04-26T18:10Z'),
        realizado: new Date('2023-04-26T18:15Z'),
        duracao: null,
        tolerancia: 20,
        titulo: 'Vacina da gripe',
        subtitulo: 'Posto de saúde do bairro',
        destaque: '',
        categoria: {
          nome: 'Vacina',
          icone: 'vaccines'
        },
        status: 'realizado',
        criticidade: 'alta'
      },
      {
        data: new Date('2023-05-09T17:00Z'),
        previsto: new Date('2023-05-09T17:00Z'),
        realizado: null,
        duracao: null,
        tolerancia: 10,
        titulo: 'Vitamina D',
        subtitulo: '2 comprimidos',
        destaque: '',
        categoria: {
          nome: 'Remédio',
          icone: 'pill'
        },
        status: 'planejado',
        criticidade: 'baixa',
        aoClicar: () => alert('Olá, mundo!')
      }
    ]
    return { perfilTimeline, listaEventos }
  }
})
</script>

<style>
:root {
  --cor-primaria: #00e01d;
}
</style>