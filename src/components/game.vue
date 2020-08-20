<template>
    <div>
        <p>HP Player {{ randomNo(1,3) }} 
            {{ player[randomNo(1,3)-1].name }}
        </p> 
        <img src="" alt="รูป">
        <hr />
            name = {{ aPlayer.name }}
            hp = {{ aPlayer.hp }}
            image = {{ aPlayer.image }}
        <hr />
        <p>HP Monster 150</p> 
        +รูป
        <button @click="start()" >Start</button>
        <button @click="attack()">Attack</button>
    </div>
</template>
<script>
export default {
    data:function(){
        return {
            aPlayer: {name: '' ,hp: 0 , image:'' },
            // ชื่อ player[1].name
            player : [{name:'Iron man',hp: 200,image:'./assets/1.jpg'},
                  {name:'Groot',hp: 350,image:'./assets/1.jpg'},
                  {name:'Docter strange',hp: 400,image:'./assets/1.jpg'}],

            monster : [{name:'Iron man',hp: 90,image:'x'},
                    {name:'Groot',hp: 180,image:'y'},
                    {name:'Docter strange',hp: 200,image:'z'}],
        };
    },
    methods:{
        randomNo: function(min, max){
            return Math.max(Math.floor(Math.random() * max) + 1, min)
        },
        start:function(){
            // 1. random Palyer 1-3 --> ชื่อ hp รูป
            this.aPlayer = this.player[this.randomNo(1, 3) - 1] 
            // {....}

            
            // 2. random Monster 1-3 --> 
        },
        attack:function(){
            // 1. playyer --> monster
            // 2. player <-- monster
            // 3. hP? <=0 ===> ?
            // 4. monster.HP <==0 ===> ?
            // 5. END GAME
        },
    },
}
</script>
<style></style>