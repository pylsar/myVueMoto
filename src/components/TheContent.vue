<template>
    <main class="content">
        <div class="content__arrow-left">
            <img  @click="left()"  src="../assets/img/arrow.svg" alt="arrow">
        </div>
        <div class="wrapper" :style="{'margin-left' : '-' + (100 * currentDucati) + '%'}" >
            <div 
                v-for="(ducati, index) in ducaties" :key="index"
                class="content__body"
            >
                <div class="content__head">
                    <span class="content__head-speed">{{ducati.speed}}</span>
                    <div class="content__head-moto"> 
                        <img :src=" require('../assets/img/' + ducati.src)" alt="ducati">
                    </div>
                </div>
                <div class="content__values">
                    <span class="content__title">Displacement</span>
                    <span class="content__text">{{ducati.displacement}}</span>
                </div>
                <div class="content__values">
                    <span class="content__title">Horse Power</span>
                    <span class="content__text">{{ducati.horsePower}}</span>
                </div>
                <div class="content__values">
                    <span class="content__title">Torque</span>
                    <span class="content__text">{{ducati.torque}}</span>
                </div>
                <div class="content__values">
                    <span class="content__title">Dry Weight</span>
                    <span class="content__text">{{ducati.dryWeight}}</span>
                </div>
                <div class="content__values">
                    <span class="content__title">Seat Height</span>
                    <span class="content__text">{{ducati.seatHeight}}</span>
                </div>
                <div class="content__values">
                    <span class="content__title">Safety</span>
                    <span class="content__text">{{ducati.safety}}</span>
                </div>
                <div class="content__sign">
                    <span>Fresh vibes.</span>
                    <span>Sporty soul.</span>
                </div>
            </div>
        </div>
        <div class="content__arrow-right">
            <img @click="right()" src="../assets/img/arrow.svg" alt="arrow"> 
        </div>
    </main>
</template>

<script>
import { TimelineMax } from "gsap";
    export default{
        name: 'TheContent',
        data(){
            return{
                currentDucati: 0,
                ducaties:[
                    {
                        'displacement': '803 cc',
                        'horsePower': '73 hp (54 kW)',
                        'torque': '67 Nm (49.0 lb-ft)',
                        'dryWeight': '175 Kg (386 lb)',
                        'seatHeight': '805 mm (31.69 in)',
                        'safety': 'ABS',
                        'src': '1.png',
                        'speed': '797'
                    },
                    {
                        'displacement': '800 cc',
                        'horsePower': '68 hp (51 kW)',
                        'torque': '70 Nm (50.0 lb-ft)',
                        'dryWeight': '185 Kg (386 lb)',
                        'seatHeight': '803 mm (31.00 in)',
                        'safety': 'ABS',
                        'src': '2.png',
                        'speed': '810'
                    },
                    {
                        'displacement': '821 cc',
                        'horsePower': '77 hp (56 kW)',
                        'torque': '73 Nm (51.0 lb-ft)',
                        'dryWeight': '170 Kg (380 lb)',
                        'seatHeight': '801 mm (31.22 in)',
                        'safety': 'ABS',
                        'src': '3.png',
                        'speed': '805'
                    }
                ]
            }
        },
        methods:{
            left(){
                if (this.currentDucati <= 0) {
                    this.currentDucati = this.ducaties.length - 1;
                }else{
                this.currentDucati--;
                }
            },
            right(){
                if (this.currentDucati >= this.ducaties.length - 1) {
                    this.currentDucati = 0;
                } else {
                    this.currentDucati++;
                }
            }
        },
        mounted(){
            let tl = new TimelineMax();
            tl
                .fromTo(".content__head-moto", 2, { x: -20000 }, { x: 0 }, "-=0.7")
                .fromTo(".content__head-speed", 1, { y: -500}, {y: 0}, "-=0.5" );
        }
    }
</script>  

<style lang="scss">
    .wrapper{
        width: 100%;
        display: flex;
        height: 80vh;
    }
    .content{
        height: 80vh;
        overflow-x: hidden;

        &__body{
            position: relative;
            min-width: 100%;
            background: #fff;
            border-radius: 50px;
            margin-top: auto;
            padding: 44px 80px 65px 80px;
        }
        &__head{
            position: absolute;
            top: -50%;
            left: 50%;
            transform: translateX(-50%);
            z-index: 10;
        }
        &__head-speed{
            color: #fff;
            font-size: 100px;
            font-weight: bold;
            position: absolute;
            top: 9%;
            left: 45%;
            transform: translateX(-50%);
            z-index: -1;
        }
        &__head-moto{
            max-width: 900px;
            min-width: 500px;
            & img{
                width: 100%;
            }
        }
        &__arrow-left{
            position: absolute;
            top: 36%;
            left: 25%;
            cursor: pointer;
            z-index: 15;
            & img{
                width: 100%;
                height: 100%;
            }
            
        }
        &__arrow-right{
            position: absolute;
            top: 36%;
            right: 25%;
            transform: rotate(180deg);
            cursor: pointer;
            z-index: 15;
            & img{
                width: 100%;
                height: 100%;
            }
            
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
            font-size: 16px;
            color: #181818;
            font-weight: 700;
            text-shadow: 1px 1px gray;
        }
        &__sign{
            font-family: 'Italianno', cursive;
            font-size: 50px;
            line-height: 1;
            width: 224px;
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

    /*ADAPTIVE*/
    @media screen and (max-width: 768px) {
        .content{
            &__arrow-left{
                width: 50px;
                height: 50px;  
                left: 10%;              
            }
            &__arrow-right{
                width: 50px;
                height: 50px;
                right: 10%;
            }
        }
    }	

    @media screen and (max-width: 672px) {
        .content{
            &__body{
                padding: 65px 80px 44px 80px;
            }
            &__head{
                top: -60%;
            }
        }
    }
    @media screen and (max-width: 550px) {
        .content{
            &__sign{
                display: none;
            }
            &__arrow-left{
                left: 5%;              
            }
            &__arrow-right{
                right: 5%;
            }
        }
    }
    @media screen and (max-width: 400px) {
        .content{
            &__head{
                top: -50%;
            }
            &__head-moto{
                min-width: 400px;
            }
            &__body{
                 padding: 65px 10px 10px 10px;
            }
        }
    }

</style>