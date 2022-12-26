<template>
<div>
<div>
    <select name="" id="" v-on:change="changeCity($event)" v-model="selectedCity">
        <option value="">==도시선택==</option>
        <option :value="city.code" :key="city.code" v-for="city in cities" >{{ city.title }}</option>
    </select>
    <select name="" id="">
        <option :value="dong.dongCode" :key="dong.dongCode" v-for="dong in selectedDongList">{{ dong.dongTitle }}</option>
    </select>
</div>
<div>
    <!-- keyup.enter 로 불필요한 함수작성을 없애준다. -->
    <input type="search" name=""  @keyup.enter="doSearch" v-model="searchText">
    <button @click="doSearch">조회</button>

</div>
</div>
</template>
<script>

export default{
    name:'',
    components:{},
    data(){
        return{
            selectedCity : '',
            cities : [
                {title : '서울' , code : '02'},
                {title : '부산' , code : '051'},
                {title : '제주' , code : '064'}
            ],
            dongList : [
                {cityCode : '02' , dongCode : '1', dongTitle : '서울 1동'},
                {cityCode : '02' , dongCode : '2', dongTitle : '서울 2동'},
                {cityCode : '02' , dongCode : '3', dongTitle : '서울 3동'},
                {cityCode : '02' , dongCode : '4', dongTitle : '서울 4동'},
                {cityCode : '051' , dongCode : '1', dongTitle : '부산 1동'},
                {cityCode : '051' , dongCode : '2', dongTitle : '부산 2동'},
                {cityCode : '051' , dongCode : '3', dongTitle : '부산 3동'},
                {cityCode : '064' , dongCode : '1', dongTitle : '제주 1동'},
                {cityCode : '064' , dongCode : '2', dongTitle : '제주 2동'},
            ],
            selectedDongList : [],
            searchText : ''
        };
    },
    setup(){},
    created(){},
    mounted(){},
    unmounted(){},
    methods:{
        changeCity(event){
            console.log(event.target.tagName)
            this.selectedDongList = this.dongList.filter(dong => dong.cityCode === this.selectedCity)
        },
        doSearch(){
            console.log(this.searchText);
        },
        checkEnter (event) {
            if(event.keyCode === 13) {
                this.doSearch()
            }
        }
    }
}
</script>