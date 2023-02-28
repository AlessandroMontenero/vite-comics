<script>
export default {
    data() {
        return {
            navItems: [
                {
                    label: 'CHARACTERS',
                    url: '#'
                },
                {
                    label: 'COMICS',
                    url: '#'
                },
                {
                    label: 'MOVIES',
                    url: '#'
                },
                {
                    label: 'TV',
                    url: '#'
                },
                {
                    label: 'GAMES',
                    url: '#'
                },
                {
                    label: 'COLLECTIBLES',
                    url: '#'
                },
                {
                    label: 'VIDEOS',
                    url: '#'
                },
                {
                    label: 'FANS',
                    url: '#'
                },
                {
                    label: 'NEWS',
                    url: '#'
                },
                {
                    label: 'SHOP',
                    url: '#'
                },
            ]
        }
    }
}
</script>

<template>
<header>
    <div class="container">
        <img src="../img/dc-logo.png" alt="">
        <ul>
            <li v-for="item in navItems" 
            :key="item.label">
                <a :href="item.url">
                    {{ item.label }}
                </a>
            </li>
        </ul>
    </div>
</header>
</template>

<style scoped>
header .container{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}

header img {
    height: 50px;
    padding: .5rem 0;
}

ul {
    list-style: none;
    display: flex;
    gap: 1rem;
}

a {
    text-decoration: none;
    color: inherit;
}
</style>
