<script>
export default {
    data() {
        return {
            activeIndex: 1,
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
            <li v-for="(item, index) in navItems" 
            :key="index">
                <a :href="item.url" :class="{active : (index == activeIndex)}" @click="activeIndex = index">
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
    padding: .4rem 0;
}

ul {
    list-style: none;
    display: flex;
    gap: 1rem;
    align-items: center;
    height: 70px;
}

li {
    height: 70px;
    display: flex;
}

a {
    text-decoration: none;
    color: inherit;
    margin-top: 25px;
}

a.active,
a:hover {
    color: rgb(60, 130, 240);
}

a.active{
    border-bottom: 4px solid rgb(60, 130, 240);
}
</style>
