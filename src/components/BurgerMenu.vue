<template>
    <div class="burger">
        <button @click="closeBurger" class="burger__icon" :class="{'isClosed' : burger}" >
            <span></span>
            <span></span>
            <span></span>
        </button>
        <div v-if="burger" class="menu">
                <h1>lksdjflksdjflkjsdf</h1>
        </div>
    </div>
</template>
<script>
    export default{
        name: 'BurgerMenu',
        data(){
            return{
                burger: false
            }
        },
        methods:{
            closeBurger(){
                this.burger = !this.burger;
            }
        }

    }
</script>

<style lang="scss">
.burger{
    &__icon{
        background: none;
        border: none;
        outline: none;
        width: 30px;
        height: 24px;
        cursor: pointer;
        position: relative;
        & span{
            display: block;
            width: 30px;
            height: 2px;
            background: #fff;
            transition: all .3s ease;
            &:first-child{
                position: absolute;
                top: 0;
                left: 0;
            }
            &:last-child{
                position: absolute;
                bottom: 0;
                left: 0;
            }
        }
    }
    .isClosed{
        & span:first-child{
            transform: rotate(45deg) translate(7px, 8px);
        }
        & span:nth-child(2) {
            opacity: 0;
        }
        & span:last-child{
            transform: rotate(-45deg) translate(7px, -8px);
        }
        
    }
}
.menu{
    position: absolute;
    top: 0;
    left: 0;
    bottom: 80vh;
    right: 0;
    background: green;
}

</style>