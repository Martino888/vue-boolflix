<template>
    <div class="container">
        <div class="main">
            <div class="logo text-uppercase  fw-bold fs-4 justify-content-start ">
                Boollflix
            </div>
            <div class="justify-content-end">
                <!-- callSearc serve per passare i dati/funzione all app vue inserendolo con la @  nel tag headerBool mentre inputMovie è la variabile che viene inclusa nei data   -->
                <input type="text" placeholder="Search movie" v-model="inputMovie" @keyup.enter="$emit('callSearch', inputMovie)">
                <button class="btn btn-outline-danger" @click="$emit('callSearch', inputMovie)" >Search</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderBool',
    data() {
        return {
            inputMovie:'',
        }
    }
}
</script>


<style scoped lang="scss">
.container{
    max-width: 100%;
    background-color: black;
    height: 60px;
}

.main{
    display: flex;
    justify-content: space-between;
}
.logo{
    color: red;

}

input{
    width: 150px;
    margin: 10px 50px;
    border-radius:10px;
    border: none;
}

</style>
