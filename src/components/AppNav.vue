<script>
export default {
    name: 'AppNav',
    data() {
        return {
            menuList: [
                {
                    name: 'Home',
                    link: '#',
                    target: '_self',
                    isActive: false
                },
                {
                    name: 'Prodotti',
                    link: '#',
                    target: '_self',
                    isActive: true
                },
                {
                    name: 'Chi Siamo',
                    link: '#',
                    target: '_self',
                    isActive: false
                },
                {
                    name: 'Contatti',
                    link: '#',
                    target: '_self',
                    isActive: false
                },
            ]
        }
    },
    methods: {
        changeMenu(index){
            // console.log('cambia il menu');
        
            this.menuList.forEach((el, i) => {
                if(index === i){
                    el.isActive = true;
                } else {
                    el.isActive = false;
                }
            })
        }
    }
}
</script>
<template>
    <nav>
        <ul>
            <li v-for="(menu, index) in menuList">
                <a :class="{active: menu.isActive}" :href="menu.link" :target="menu.target" @click.prevent="changeMenu(index)">{{ menu.name }}</a>
            </li>
        </ul>
    </nav>
</template>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
nav {
    ul {
        margin: 0;
        list-style: none;
        display: flex;
        justify-content: center;
    }

    li {
        a {
            display: inline-block;
            padding: 1.125rem;
            color: $text-color;

            &.active {
                background-color: $secondary-color;
            }
          
            &:hover {
                background-color: darken($secondary-color, 10%);
            }
        }
    }

}
</style>