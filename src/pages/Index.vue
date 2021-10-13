<template>
  <q-page id="portafolio" class="q-pa-none q-ma-none">
    <!-- Rows para fotos e info -->
    <!-- Primer fila -->
    <div  class="row text-center" >
      <div  class="col-12 col-md-1"></div>
      <div class="col-12 col-md-5 q-pa-lg text-left">
        <div class="">
          <p class="bg-black q-ma-none text-white uppercase"> <strong class="text-green">LOREM</strong> IPSUM IS SIMPLY DUMMY TEXT <strong class="text-green"> THE PRINTING AND TYPESETTING INDUSTRY </strong>. LOREM IPSUM HAS BEEN THE INDUSTRY'S STANDARD DUMMY <strong class="text-green">TEXT EVER SINCE THE 1500</strong> </p>
        </div>
      </div>

      <div class="col-12 col-md-5 q-pa-lg">
        <div class=" img-hover-zoom" style="height:100%" @click="()=>{medium = true; link = 'https://fondosmil.com/fondo/2258.jpg'}">
          <q-img width="100%" height="100%" class="rounded-borders img" src="https://fondosmil.com/fondo/2258.jpg" />
        </div>
      </div>

      <div class="col-12 col-md-1"></div>

    </div>
    <!-- Segunda fila -->
    <div  class="row text-center" >

      <div class="col-12 col-md-1"></div>

      <div class="col-12 col-md-5 q-pa-lg">
        <div class="videoContainer img-hover-zoom" style="height:100%" @click="()=>{mediumVideo = true; linkVideo = 'https://www.youtube.com/embed/xcJtL7QggTI'}">
          <q-img width="100%" height="100%" class="rounded-borders img" src="https://img.youtube.com/vi/xcJtL7QggTI/maxresdefault.jpg" />
          <img alt="play" class="playBtn" src="https://i.pinimg.com/originals/a1/1b/ab/a11babe56eada90b29709f82bbf7dec4.png" >
        </div>
      </div>

      <div class="col-12 col-md-5 q-pa-lg">
        <div class="videoContainer img-hover-zoom" style="height:100%" @click="()=>{mediumVideo = true; linkVideo = 'https://www.youtube.com/embed/IBfQXYe0-Lc'}">
          <q-img width="100%" height="100%" class="rounded-borders img" src="https://img.youtube.com/vi/IBfQXYe0-Lc/maxresdefault.jpg" />
          <img alt="play" class="playBtn" src="https://i.pinimg.com/originals/a1/1b/ab/a11babe56eada90b29709f82bbf7dec4.png" >
        </div>
      </div>

      <div class="col-12 col-md-1"></div>

    </div>
    <!-- Tercer fila -->
    <div  class="row text-center" >
      <div class="col-12 col-md-1"></div>

      <div class="col-12 col-md-5 q-pa-lg">
        <div class=" img-hover-zoom" style="height:100%" @click="()=>{medium = true; link = 'https://i.pinimg.com/originals/e1/00/1e/e1001e86903d5fccba2a7e83a0547bd4.jpg'}">
          <q-img width="100%" height="100%" class="rounded-borders img" src="https://i.pinimg.com/originals/e1/00/1e/e1001e86903d5fccba2a7e83a0547bd4.jpg" />
        </div>
      </div>

      <div class="col-12 col-md-5 q-pa-lg">
        <div class=" img-hover-zoom" style="height:100%" @click="()=>{medium = true; link = 'https://i.pinimg.com/originals/33/8a/55/338a55304e6dc72ef9258968ce045e8d.jpg'}">
          <q-img width="100%" height="100%" class="rounded-borders img" src="https://i.pinimg.com/originals/33/8a/55/338a55304e6dc72ef9258968ce045e8d.jpg" />
        </div>
      </div>

      <div class="col-12 col-md-1"></div>

    </div>
    <!-- Cuarta fila -->
    <div  class="row text-center" >
      <div class="col-12 col-md-1"></div>

      <div class="col-12 col-md-5 q-pa-lg">
        <div class=" img-hover-zoom" style="height:100%" @click="()=>{medium = true; link = 'https://i.pinimg.com/originals/e1/00/1e/e1001e86903d5fccba2a7e83a0547bd4.jpg'}">
          <q-img width="100%" height="100%" class="rounded-borders img" src="https://i.pinimg.com/originals/e1/00/1e/e1001e86903d5fccba2a7e83a0547bd4.jpg" />
        </div>
      </div>

      <div class="col-12 col-md-5 q-pa-lg">
        <div class=" img-hover-zoom" style="height:100%" @click="()=>{medium = true; link = 'https://fondosmil.com/fondo/2257.jpg'}">
          <q-img width="100%" height="100%" class="rounded-borders img" src="https://fondosmil.com/fondo/2257.jpg" />
        </div>
      </div>

      <div class="col-12 col-md-1"></div>
    </div>

    <!-- Row para contacto -->
    <div class="row text-center items-baseline" id="contacto" >
      <div class="col-12 col-md-1"></div>
      <div class="col-12 col-md-5 q-pa-lg text-left ">
          <p class="bg-black q-ma-none text-white"> CONTACTO </p>
          <p class="bg-black q-ma-none text-white mail"> EMAIL@CONTACTO.COM</p>
      </div>

      <div class="col-12 col-md-5 q-pa-lg">
        <q-form v-on:submit="sendMessage" >
          <div class="img-hover-zoom bg-black text-left">
            <h5 class="text-white q-my-none">Nombre</h5>
            <q-input ref="input1" dense square dark color="white" v-model="nombre" outlined  class="bg-black q-mb-xs input" lazy-rules :rules="[val => !!val || 'Ingrese su nombre']"/>
            <h5 class="text-white q-my-none">Correo electronico</h5>
            <q-input ref="input2" dense square dark color="white" v-model="correo" outlined class="bg-black q-mb-xs input" lazy-rules :rules="[val => !!val || 'Ingrese un correo']"/>
            <h5 class="text-white q-my-none">Mensaje</h5>
            <q-input ref="input3" dense square type="textarea"  dark color="white" v-model="mensaje" outlined class="q-mb-xs input" lazy-rules :rules="[val => !!val || 'Ingrese un mensaje']"/>
            <q-btn outline rounded color="white" type="submit" class="bg-white text-black q-px-lg" label="Enviar" />
          </div>
        </q-form>
      </div>
      <div class="col-12 col-md-1"></div>
    </div>
    <!-- Dialog fotos -->
    <q-dialog
      v-model="medium"
    >
      <q-card style="width: 900px; max-width: 1000px;">
        <q-card-section>
          <q-img width="100%"  class="rounded-borders img" :src=link />
        </q-card-section>
      </q-card>
    </q-dialog>
        <!-- Dialog video -->
    <q-dialog
      v-model="mediumVideo"
    >
      <q-card style="width: 900px; max-width: 1000px;">
        <q-card-section>
           <iframe width="100%" height="500" :src=linkVideo title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </q-card-section>
      </q-card>
    </q-dialog>
  </q-page>
</template>

<script>

export default {
  name: 'PageIndex',
  data: function () {
    return {
      mensaje: '',
      nombre: '',
      correo: '',
      medium: false,
      mediumVideo: false,
      link: '',
      linkVideo: ''
    }
  },
  methods: {
    sendMessage: function () {
      console.log('MENSAJE ENVIADO')
      this.reset()
    },
    reset: function () {
      this.nombre = ''
      this.correo = ''
      this.mensaje = ''
      this.$refs.input1.resetValidation()
      this.$refs.input2.resetValidation()
      this.$refs.input3.resetValidation()
    }
  }
}
</script>

<style lang="sass" scoped>

.img-hover-zoom:hover .playBtn
  color: #00000000
  transform: scale(1.2)
  transition: 0.45s all ease-in-out

.videoContainer
  position: relative

.playBtn
  position: absolute
  width: 96px
  height: 96px
  left: 50%
  top: 50%
  margin-left: -48px /*half of the width */
  margin-top: -48px /*half of the height */
  transition: 0.45s all ease-in-out

.img-hover-zoom
  overflow: hidden
  margin: 0 auto
  display:table
  border-radius: 2px

.img
  transition: 0.45s all ease-in-out
  border-radius: 2px

.img-hover-zoom:hover .img
  transform: scale(1.1)

@import url('https://fonts.googleapis.com/css?family=Black+Han+Sans')
p
  font-family: 'Black Han Sans'
  font-size: 30px
  font-weight: 100

@import url('https://fonts.googleapis.com/css2?family=Lato:wght@700&display=swap')
h5
  font-family: 'Lato', sans-serif
  font-size: 20px

.mail
  font-size: 28px

#portafolio
  scroll-margin-top: 5rem
</style>
