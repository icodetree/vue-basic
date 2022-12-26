<template>
<div>
    <div>{{htmlString}}</div>
    <div v-html="htmlString"></div>
    <input type="text" v-model="userId">
    <button @click="myfunction">클릭</button>
    <button @click="changeData">변경</button>
    <br>
    <input type="text" v-model.number="num1"> +
    <input type="text" v-model.number="num2"> =
    <span>{{ num1 + num2 }}</span>
    <br>
    <select v-model="selectedCity">
        <option value=""></option>
        <option value="02">서울</option>
        <option value="064">제주</option>
        <option value="051">부산</option>
    </select>
    <br>
    <div>
        <input type="checkbox" id="html" value="html" v-model="favoriteLang">
        <label for="html">HTML</label>
    </div>
    <div>
        <input type="checkbox" id="css" value="CSS" v-model="favoriteLang">
        <label for="css">CSS</label>
    </div>
    <div>
        <input type="checkbox" id="js" value="JS" v-model="favoriteLang">
        <label for="js">Javascript</label>
    </div>
    <p>선택한 지역 : {{ favoriteLang }}</p>
    <br>
    <div>
        <input type="radio" id="html1" value="html" v-model="radioLeng">
        <label for="html1">HTML</label>
    </div>
    <div>
        <input type="radio" id="css1" value="css" v-model="radioLeng">
        <label for="css1">CSS</label>
    </div>
    <div>
        <input type="radio" id="js1" value="js" v-model="radioLeng">
        <label for="js1">Javascript</label>
    </div>
    <p>선택한 지역 : {{ radioLeng }}</p>
    <br>
    <input type="text" v-bind:value="userName" readonnly />
    <br>
    <img :src="imgSrc" alt="" >
    <br>
    <input type="search"   v-model="text1">
    <!-- input 값이 비어있을때 비활성화 -->
    <button :disabled="text1 === ''">조회</button>
</div>
</template>
<script>

export default{
    components:{},
    data(){
        return{
            htmlString:'<p style="color:red">빨간색 문자</p>',
            userId : 'BHY',
            num1 : 0,
            num2 : 0,
            selectedCity : '051',
            favoriteLang : [], // 체크박스는 배열로
            radioLeng : '', //라디오버튼은 문자열로,
            userName : '변호영',
            imgSrc : 'https://www.google.com/logos/doodles/2022/seasonal-holidays-2022-6753651837109831.4-s.png',
            text1 : ''
        };
    },
    setup(){},
    created(){},
    mounted(){},
    unmounted(){},
    methods:{
        myfunction () {
            console.log(this.userId)
        },
        changeData () {
            this.userId = 'Funcoding'
        }
    }
}
</script>