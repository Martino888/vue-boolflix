<template>
    <div class="container">
        <div class="main">
            <div class="logo text-uppercase  fw-bold fs-4 justify-content-start ">
                Boollflix
            </div>
            <form action="" class="justify-content-end">
                <input type="text">
                <button class="btn btn-outline-danger" >Cerca</button>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HeaderBool'
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
