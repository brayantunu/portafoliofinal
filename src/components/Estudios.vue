<template>
  <!-- https://daisyui.com/images/stock/photo-1635805737707-575885ab0820.jpg -->
  <div class="hero min-h-screen">
    <div class="hero-content flex-col lg:flex-row">

      <div class="card rounded-lg">
        <img src="../assets/brayan.jpeg" class="photo" alt="">
      </div>
      <!-- <img src="../assets/brayan.jpeg" class="rounded-lg shadow-2xl xlx imagen2" /> -->
      <div class="background-overlay">
        <div class="contenedor">
          <h1>HI, I'M BRAYAN<span>&#160;</span></h1>
        </div>
        <p class="py-6">WEB DEVELOPER</p>
        <button class="bn">Download CV</button>
      </div>
    </div>
  </div>
  
  <div class="collapse bg-base-200">
  <input type="radio" name="my-accordion-1" checked="checked" /> 
  <div class="collapse-title text-xl font-medium flex-initial">
  <p class="Informacion">SOBRE MI </p>
  </div>
  <div class="collapse-content"> 
    <div class="container-estudios">
    <div class="image-container">
      <img src="../assets/spiderman.avif" alt="Mi imagen" class="animated-image">
    </div>
    <div class="info-container">
      <div class="con-info">
        <h2>Soy Brayan Tunubala</h2>
        
        <p class="sobremi">
          Soy un apasionado de la tecnología con un enfoque especial en el desarrollo de software, y tambien tengo habilidades en la gestión de documentación y el manejo avanzado de paquete office. Mi objetivo se centra en la colaboración, la excelencia y la responsabilidad, siempre buscando oportunidades para crecer y aprender de manera continua. Me entusiasma aplicar mis habilidades y conocimientos, siendo creativo y una mentalidad abierta para enfrentar nuevos desafíos. Estoy dispuesto a asumir responsabilidades y colaborar de manera efectiva con otros profesionales para contribuir en equipo.
        </p>
      </div>

    </div>
  </div>
  </div>
</div>
<div class="collapse bg-base-200">
  <input type="radio" name="my-accordion-1" /> 
  <div class="collapse-title text-xl font-medium">
    Click to open this one and close others
  </div>
  <div class="collapse-content"> 
    <p>hello</p>
  </div>
</div>
<div class="collapse bg-base-200">
  <input type="radio" name="my-accordion-1" /> 
  <div class="collapse-title text-xl font-medium">
    Click to open this one and close others
  </div>
  <div class="collapse-content"> 
    <p>hello</p>
  </div>
</div>

  
  
</template>
<script>
export default {
  name: "EstudiosV"
}
</script>
<style>
/* card foto presentacion */

.collapse{
 width: 98%;
}
.card {
  background: #07182E;
  position: relative;
  display: flex;
  place-content: center;
  place-items: center;
  overflow: hidden;
  border-radius: 20px;
}

.card .photo {
  z-index: 1;
  padding: 10px;

}

.card::before {
  content: '';
  position: absolute;
  width: 100px;
  background-image: linear-gradient(180deg, rgb(0, 183, 255), rgb(255, 48, 255));
  height: 130%;
  animation: rotBGimg 3s linear infinite;
  transition: all 0.2s linear;
}

@keyframes rotBGimg {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}

.card::after {
  content: '';
  position: absolute;
  background: #07182E;
  ;
  inset: 5px;
  border-radius: 15px;
}

/* .card:hover:before {
  background-image: linear-gradient(180deg, rgb(81, 255, 0), purple);
  animation: rotBGimg 3.5s linear infinite;
} */





/* presentacion  */
.hero {
  position: relative;
}

.hero::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url("https://daisyui.com/images/stock/photo-1635805737707-575885ab0820.jpg");
  background-size: cover;
  background-position: center;
  z-index: -1;
}

.hero-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 2rem;
  color: #ffffff;

}

.hero-content .photo {
  border-radius: 20px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
}

.hero-content h1 {
  font-size: 2.5rem;
  font-weight: bold;
  margin-top: 1.5rem;
  margin-bottom: 1rem;
}

.hero-content p {
  font-size: 1.2rem;
  line-height: 1.5;
  margin-bottom: 1.5rem;
}

.typing-animation {
  display: inline-block;
  overflow: hidden;
  white-space: nowrap;
  animation: typing 4s steps(6), wait 3s, erasing 2s steps(23) 7s, typing 4s steps(25) 9s;
  border-right: 0.15em solid orange;
}

@keyframes typing {
  from {
    width: 0;
  }

  to {
    width: 100%;
  }
}

@keyframes erasing {
  from {
    width: 100%;
  }

  to {
    width: 0;
  }
}

.contenedor {
  position: relative;
  z-index: 2;
}

.contenedor h1 {
  color: #ffffff;
}

.contenedor span {
  display: inline-block;
  width: 0;
  animation: cursor-animation 0.5s infinite;
}

@keyframes cursor-animation {
  50% {
    opacity: 0;
  }
}

/* boton descargar cv */
button {
  /* --border-radius: 30px; */
  --border-width: 3px;
  appearance: none;
  position: relative;
  padding: 1em 2em;
  border: 0;
  /* background-color: #212121; */
  font-family: "Roboto", Arial, "Segoe UI", sans-serif;
  font-size: 18px;
  font-weight: 500;
  color: #ffff;
  z-index: 2;
}

button::after {
  --m-i: linear-gradient(#000, #000);
  --m-o: content-box, padding-box;
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  padding: var(--border-width);
  background-image: conic-gradient(#ff0080,
      #ff0080,
      #ff0080,
      #ff0080,
      #ff0080,
      #ff0080,
      #ff0080);
  -webkit-mask-image: var(--m-i), var(--m-i);
  mask-image: var(--m-i), var(--m-i);
  -webkit-mask-origin: var(--m-o);
  mask-origin: var(--m-o);
  mask-clip: var(--m-o);
  mask-composite: exclude;
  -webkit-mask-composite: destination-out;
  filter: hue-rotate(0);
  animation: rotate-hue634 linear 500ms infinite;
  animation-play-state: paused;
  border-radius: 30px;
  border-color: #000;
}

button:hover::after {
  animation-play-state: running;
  border-radius: 10px;
}

@keyframes rotate-hue634 {
  to {
    filter: hue-rotate(1turn);
  }
}

button,
button::after {
  box-sizing: border-box;
  border-radius: 30px;
}

button:active {
  --border-width: 5px;
}

.bn {
  padding: 0.9em 1.6em;
  border: none;
  outline: none;
  color: #FFF;
  font-family: inherit;
  font-weight: 500;
  font-size: 17px;
  cursor: pointer;
  position: relative;
  z-index: 0;
  border-radius: 32px;
}

.bn::after {
  content: "";
  z-index: -1;
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: rgb(46, 46, 46);
  left: 0;
  top: 0;
  border-radius: 10px;
}

.bn::before {
  content: "";
  background: linear-gradient(45deg,
      #07d888, #e40851, #2f00ff, #00ff37,
      #ec0808, #2600ff, #0bd157, #2f00ff);
  position: absolute;
  top: -2px;
  left: -2px;
  background-size: 600%;
  z-index: -1;
  width: calc(100% + 4px);
  height: calc(100% + 4px);
  filter: blur(8px);
  animation: glowing345 20s linear infinite;
  transition: opacity .3s ease-in-out;
  border-radius: 20px;
  opacity: 0;
}

@keyframes glowing345 {
  0% {
    background-position: 0 0;
  }

  50% {
    background-position: 400% 0;
  }

  100% {
    background-position: 0 0;
  }
}

.bn:hover::before {
  opacity: 1;
}

.bn:active:after {
  background: transparent;
}

.bn:active {
  color: #000;
  font-weight: bold;
}



/* sobre mi informacion detallada */
.container-estudios {
  display: flex;
  border-radius: 50px;  
 margin-bottom: 30px;
}

.image-container {
  width: 40%;
  margin: 20px auto;
}

.animated-image {
  border: 2px solid transparent;
  border-radius: 50%;
  animation: animateBorder 3s linear infinite;
  margin: auto;
  width: 60%;
}



@keyframes animateBorder {
  0% {
    border: 2px solid transparent;
    box-shadow: 0 0 0 #0000ff;
    /* Color azul transparente */
  }

  50% {
    border: 2px solid #0000ff;
    /* Color azul sólido */
    box-shadow: 0 0 10px #0000ff;
    /* Color azul sólido y desenfoque de 10px */
  }

  100% {
    border: 2px solid transparent;
    box-shadow: 0 0 0 #0000ff;
    /* Color azul transparente */
  }
}

.sobremi{
  margin-top: 20px;
}

.Informacion{
  text-align: center;
}
</style>