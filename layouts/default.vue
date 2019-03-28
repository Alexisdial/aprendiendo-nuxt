<template>
    <div>
        <navbar/>
        <Nuxt /> <!--hace referencia a todo el contenido -->
        esto es un footer
    </div>
</template>

<script>
import navbar from '../Components/navbar'
export default {
    components: {navbar},
}
</script>

