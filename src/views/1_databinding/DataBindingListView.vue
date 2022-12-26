<template>
<div>
    <div>
        <select name="" id="">
            <option :value="city.code" :key="city.code" v-for="city in cities">{{ city.title }}</option>
        </select>
    </div>

    <div>
        <table>
            <thead>
                <tr>
                    <th>번호</th>
                    <th>제품명</th>
                    <th>가격</th>
                    <th>수량</th>
                    <th>합계</th>
                </tr>
            </thead>
            <tbody>
                <tr :key="drink.drinkId" v-for="drink in drinkList">
                <td>{{drink.drinkId}}</td>
                <td>{{drink.drinkName}}</td>
                <td>{{drink.price}}</td>
                <td><input type="number" v-model="drink.qty"></td>
                <td>{{ drink.price * drink.qty }}</td>
                </tr>
            </tbody>
        </table>
    </div>
    <div :class="{ 'text-red' : hasError, active : isActive}">
        클래스바인딩
    </div>

    <div :style="style1">스타일 바인딩은 객체형식으로 등록한다.</div>
    <button @click="style1.color='blue'">색상변경</button>
</div>
</template>
<script>

export default{
    name:'',
    components:{},
    data(){
        return{
            cities : [
                {title : '서울' , code : '02'},
                {title : '부산' , code : '051'},
                {title : '제주' , code : '064'}
            ],
            drinkList : [
                {
                    drinkId : '1',
                    drinkName : '코카콜라',
                    price : 700,
                    qty : 1
                },
                {
                    drinkId : '2',
                    drinkName : '오렌지주스',
                    price : 1200,
                    qty : 1
                },
                {
                    drinkId : '3',
                    drinkName : '커피',
                    price : 500,
                    qty : 1
                },
            ],

            isActive : false,
            hasError : false,
            style1 : {
                color : 'red',
                fontSize : '30px'
            }
        };
    },
    setup(){},
    created(){},
    mounted(){},
    unmounted(){},
    methods:{}
}
</script>
<style scoped>
.active {
    background-color : greenyellow;
    font-weight:bold;
}
.text-red {
    color:#f00;
}
</style>