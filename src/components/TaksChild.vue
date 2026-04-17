<script setup>
defineProps(['id', 'descricao', 'status'])
defineEmits(['editar', 'excluir'])
</script>

<template>
<li>
    {{ descricao }}
    <a href="#" @click.prevent="$emit('excluir', id)">Excluir</a>
    <a href="#" @click.prevent="$emit('editar', id)">Editar</a>
</li>
<li>
    {{ status }}
    <a href="#" @click.prevent="$emit('marcarConcluida', id)">Marcar concluida</a>
</li>
</template>

<style scoped>

</style>