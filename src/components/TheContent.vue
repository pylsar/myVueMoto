<template>
    <main class="content">

        <div
            v-show="bike===0" 
            class="content__body"
            >
            <div class="content__head">
                <img  @click="left" v-if="bike !== 0" class="content__head-left" src="../assets/img/arrow.svg" alt="arrow">
                <span class="content__head-speed">797</span>
                <div class="content__head-moto"> 
                    <img 
                        src="../assets/img/1.png" 
                        alt="buggati"  
                    >
                </div>
                <img @click="right"  class="content__head-right" src="../assets/img/arrow.svg" alt="arrow"> 
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Horse Power</span>
                <span class="content__tetx">73 hp (54 kW)</span>
            </div>
            <div class="content__values">
                <span class="content__title">Torque</span>
                <span class="content__tetx">67 Nm (49.0 lb-ft)</span>
            </div>
            <div class="content__values">
                <span class="content__title">Dry Weight</span>
                <span class="content__tetx">175 Kg (386 lb)</span>
            </div>
            <div class="content__values">
                <span class="content__title">Seat Height</span>
                <span class="content__tetx">805 mm (31.69 in)</span>
            </div>
            <div class="content__values">
                <span class="content__title">Safety</span>
                <span class="content__tetx">ABS</span>
            </div>
            <div class="content__sign">
                <span>Fresh vibes.</span>
                <span>Sporty soul.</span>
            </div>
        </div>
        <div
            v-show="bike===1" 
            class="content__body"
            >
            <div class="content__head">
                <img  @click="left" class="content__head-left" src="../assets/img/arrow.svg" alt="arrow">
                <span class="content__head-speed">810</span>
                <div class="content__head-moto"> 
                    <img 
                        src="../assets/img/2.png" 
                        alt="buggati"
                    >
                </div>    
                <img @click="right"  class="content__head-right" src="../assets/img/arrow.svg" alt="arrow"> 
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">821 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Horse Power</span>
                <span class="content__tetx">109 hp (80 kW)</span>
            </div>
            <div class="content__values">
                <span class="content__title">Torque</span>
                <span class="content__tetx">86 Nm (63 lb-ft)</span>
            </div>
            <div class="content__values">
                <span class="content__title">Dry Weight</span>
                <span class="content__tetx">180.5 Kg (398 lb)</span>
            </div>
            <div class="content__values">
                <span class="content__title">Seat Height</span>
                <span class="content__tetx">805 mm (31.69 in)</span>
            </div>
            <div class="content__values">
                <span class="content__title">Safety</span>
                <span class="content__tetx">ABS</span>
            </div>
            <div class="content__sign">
                <span>Fresh vibes.</span>
                <span>Sporty soul.</span>
            </div>
        </div>
                <div
            v-show="bike===2" 
            class="content__body"
            >
            <div class="content__head">
                <img  @click="left"  class="content__head-left" src="../assets/img/arrow.svg" alt="arrow">
                <span class="content__head-speed">832</span>
                <div class="content__head-moto">
                    <img 
                        src="../assets/img/3.png" 
                        alt="buggati"
                    >
                </div>
                <img @click="right" v-if=" bike !==2" class="content__head-right" src="../assets/img/arrow.svg" alt="arrow"> 
            </div>
            <div class="content__values">
                <span class="content__title">Displacement</span>
                <span class="content__tetx">803 cc</span>
            </div>
            <div class="content__values">
                <span class="content__title">Horse Power</span>
                <span class="content__tetx">73 hp (54 kW)</span>
            </div>
            <div class="content__values">
                <span class="content__title">Torque</span>
                <span class="content__tetx">67 Nm (49.0 lb-ft)</span>
            </div>
            <div class="content__values">
                <span class="content__title">Dry Weight</span>
                <span class="content__tetx">175 Kg (386 lb)</span>
            </div>
            <div class="content__values">
                <span class="content__title">Seat Height</span>
                <span class="content__tetx">805 mm (31.69 in)</span>
            </div>
            <div class="content__values">
                <span class="content__title">Safety</span>
                <span class="content__tetx">ABS</span>
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
            top: 9%;
            left: 45%;
            transform: translateX(-50%);
            z-index: -1;
        }
        &__head-moto{
            max-width: 900px;
            & img{
                width: 100%;
            }
        }
        &__head-left{
            position: absolute;
            top: 40%;
            left: 5%;
            cursor: pointer;
            z-index: 15;
        }
        &__head-right{
            position: absolute;
            top: 40%;
            right: 5%;
            transform: rotate(180deg);
            cursor: pointer;
            z-index: 15;
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

</style>