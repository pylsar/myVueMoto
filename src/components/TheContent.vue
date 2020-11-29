<template>
    <main class="content">

        <div
            v-if="bike===0" 
            class="content__body"
            >
            <div class="content__head">
                <img  @click="left" v-if="bike !== 0" class="content__head-left" src="../assets/img/arrow.svg" alt="">
                <span class="content__head-speed">797</span>
                <img src="../assets/img/1.png" alt="buggati">
                <img @click="right"  class="content__head-right" src="../assets/img/arrow.svg" alt=""> 
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__sign">
                <span>Fresh vibes.</span>
                <span>Sporty soul.</span>
            </div>
        </div>
                <div
            v-if="bike===1" 
            class="content__body"
            >
            <div class="content__head">
                <img  @click="left" class="content__head-left" src="../assets/img/arrow.svg" alt="">
                <span class="content__head-speed">810</span>
                <img src="../assets/img/2.png" alt="buggati">
                <img @click="right"  class="content__head-right" src="../assets/img/arrow.svg" alt=""> 
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__sign">
                <span>Fresh vibes.</span>
                <span>Sporty soul.</span>
            </div>
        </div>
                <div
            v-if="bike===2" 
            class="content__body"
            >
            <div class="content__head">
                <img  @click="left"  class="content__head-left" src="../assets/img/arrow.svg" alt="">
                <span class="content__head-speed">832</span>
                <img src="../assets/img/3.png" alt="buggati">
                <img @click="right" v-if=" bike !==2" class="content__head-right" src="../assets/img/arrow.svg" alt=""> 
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__sign">
                <span>Fresh vibes.</span>
                <span>Sporty soul.</span>
            </div>
        </div>

    </main>
</template>

<script>
    export default{
        name: 'TheContent',
        data(){
            return{
                bike: 0,
            }
        },
        methods:{
            left(){
                this.bike = this.bike - 1;
            },
            right(){
                this.bike = this.bike + 1;
            }
        }
    }
</script>  

<style lang="scss">
    .content{
        position: relative;
        &__head{
            position: absolute;
            top: -20%;
            left: 50%;
            transform: translate(-50%,-50%);
            z-index: 10;
        }
        &__head-speed{
            color: #fff;
            font-size: 100px;
            font-weight: bold;
            position: absolute;
            top: 24%;
            left: 45%;
            transform: translateX(-50%);
            z-index: -1;
        }
        &__head-left{
            position: absolute;
            top: 40%;
            left: 10%;
            cursor: pointer;
        }
        &__head-right{
            position: absolute;
            top: 40%;
            right: 15%;
            transform: rotate(180deg);
            cursor: pointer;
        }
        &__body{
            width: 96%;
            margin: 0 auto;
            background: #fff;
            border-radius: 50px;
            margin-top: auto;
            padding: 44px 80px 65px 80px;
        }
        &__values{
            display: flex;
            flex-direction: column;
            margin-bottom: 10px;
        }
        &__title{
            font-size: 12px;
            color: #181818;
        }
        &__text{
            font-size: 24px;
            color: #181818;
            font-weight: 700;
        }
        &__sign{
            border: 1px solid blue;
            width: 500px;
            position: absolute;
            right: 80px;
            bottom: 65px;
            & span:first-child{
                text-align: left;
                display: block;
            }
            & span:last-child{
                text-align: right;
                display: block;
            }
        }
    }
</style>