<template>
    <nav class="uk-navbar-container" uk-navbar>
        <div class="uk-navbar-center">

            <ul class="uk-navbar-nav">
                <!-- <li v-for="(link, index) in links :index='link.id'> -->
                <li v-for="link in links" v-bind:key="link.id">
                    <router-link :to="link.href">{{ link.title }}</router-link>
                </li>
            </ul>

        </div>
    </nav>
</template>

<script>
    export default {
      data() {
          return {
              links: [
                {
                    title: "Main",
                    href: "/",
                    id: 1
                },
                {
                    title: "Blog",
                    href: "/blog",
                    id: 2
                }
              ],
          }
      }
    }
</script>

<style scoped>
</style>