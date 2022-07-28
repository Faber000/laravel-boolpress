<template>
  <header>
    <div class="container">
        <nav>
            <ul>
                <li><router-link :to="{ name: 'home' }">Home</router-link></li>
                <li><router-link :to="{ name: 'categories' }">Categorie</router-link></li>
                <li><a href="/admin/home">Area Riservata</a></li>
            </ul>
        </nav>
    </div>
  </header>
</template>

<script>
export default {
    name: 'BaseHeader',
}
</script>

<style>
</style>