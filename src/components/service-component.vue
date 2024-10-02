<template>
  <div class="card-rotate">
    <div class="inner-card">
      <div class="service black front">
        <img :src="imgPath" alt="">
        <h3>{{title}}</h3>
      </div>
      <div class="service back">
        <h4>{{title}}</h4>
        <p>{{description}}</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.card-rotate {
  height: 296px;
  max-width: 400px;
  perspective: 1000px;
  cursor: pointer;
  flex-grow: 1;
  width: 100%;
  box-sizing: border-box;
  background:  #1B1C1E;
  margin-bottom: 20px;
  margin-right: 20px;
  overflow: hidden;
  border-radius: 10px;
  @media only screen and (max-width: 1250px){
    width: 400px;
  }
  .card-rotate:nth-child(3), .card-rotate:nth-child(4){
    width: 506px;
    flex-grow: 0;
    max-width: 506px;
    @media only screen and (max-width: 1250px){
      width: 400px;
    }
  }
}
.inner-card{
  width: 100%;
  height: 100%;
  transform-style: preserve-3d;
  transition: transform 0.5s;
}
.front, .back{
  width: 100%;
  height: 100%;
  position: absolute;
  backface-visibility: hidden;
  display: flex;
  flex-direction: column;
}
.back{
  transform: rotateY(180deg);
  background-color: #1B1C1E;
  border-radius: 10px;
  padding: 20px;
  box-sizing: border-box;
  color:white;
  h4{
    font-size: 18px;
    margin: 0 auto;
  }
}
.card-rotate:hover .inner-card {
  transform: rotateY(180deg);
}

  .service{
    h3{
      color:  #FFF;
      font-family: "Soyuz Grotesk",sans-serif;
      font-size: 30px;
      font-style: normal;
      font-weight: 700;
      line-height: normal;
      width: 61%;
      margin-left: 40px;
      margin-top: 50px;
      z-index: 100;
    }
    a{
      color:  #DE4C2F;
      font-family: SVN-Gilroy,sans-serif;
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: normal;
      text-decoration-line: underline;
      margin-left: 53px;
    }
    img{
      width: 100%;
      position: absolute;
      bottom: 0;
    }
  }
  .card-rotate:last-child, .card-rotate:nth-child(3){
    margin-right: 0;
    @media only screen and (max-width: 1250px){
      margin-right: 20px;
    }

  }
  .card-rotate:nth-child(4){
    img{
      @media only screen and (min-width: 865px){
        bottom: -100px;
      }
    }
  }
  .card-rotate:nth-child(3), .card-rotate:nth-child(4){
    border-radius: 10px;
    width: 298px;
    flex-grow: 0;
    background:linear-gradient(114deg, #CB422B 1.43%, #771515 101.61%);
    @media only screen and (max-width: 1250px){
      width: 400px;
    }
    .back{
      background:linear-gradient(114deg, #CB422B 1.43%, #771515 101.61%);
    }
    a{
      color:#fff;
    }
  }
  .service.black{
    border-radius: 10px;
    border: 1px solid #535353;


  }



</style>
<script setup lang="ts">
defineProps(
  {
    imgPath: String,
    link: String,
    title:String,
    description:String
  }
);

</script>