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
            :key="index"
            :class="{active : (index == activeIndex)}">
                <a :href="item.url"  @click="activeIndex = index">
                    <h3>{{ item.label }}</h3>
                </a>
            </li>
        </ul>
    </div>
</header>
</template>

<style lang="scss" scoped>
header {
    .container{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }
    
    img {
        height: 70px;
        padding: .4rem 0;
    }
}


ul {
    display: flex;
    gap: 1rem;
    align-items: center;
    height: 100px;
    
    li {
        display: flex;
        align-items: center;
        height: 100%;
        box-sizing: border-box;
        h3 {
            padding: 0;
            margin: 0;
        }
    }
    
    li.active,
    li:hover {
        color: rgb(60, 130, 240);
    }
    
    li.active{
        border-bottom: 4px solid rgb(60, 130, 240);
    }

    a {
        padding: 40px 0;
        text-decoration: none;
        color: inherit;
        align-self: stretch;
    }
}
</style>
