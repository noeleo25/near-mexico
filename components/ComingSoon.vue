<template>
    <div>
        <div class="cs-bg">
            <img  class="map" src="~/assets/map-bg.svg">
            <div class="over">
                <img class="logo" src="~/assets/logo.svg">
                <h1> Coming Soon </h1>
            </div>
        </div>
        
    </div>
</template>

<style scoped>
html{
    background-color: black;
}
.cs-bg{
    color: #fff;
    display: flex;
    align-content: center;
    justify-content: center;
    position: relative;
}
.map{
    width: 100%;
    max-width: 910px;
}
.over{
    position: absolute;
    /*width: 100%;
    height: 100%;*/
    text-align: center;
    top: 50%;
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
}
h1{
    font-size: 7vw;
    font-family: 'Open Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    text-align: center;
    text-transform: uppercase;
    
}
</style>