<template>
    <section class="d-flex min-vh-100 justify-content-center align-items-center loader-bg">
        <div class="loader"></div>
    </section>
</template>
<style scoped>
.loader-bg{
  background: #42307D;
}
.loader {
  width: 75px;
  aspect-ratio: 1; 
  display: grid;
}
.loader:before,
.loader:after {
  content: "";
  grid-area: 1/1;
  width: 35px;
  aspect-ratio: 1;
  box-shadow: 0 0 0 3px #fff inset;
  filter: drop-shadow(40px 40px 0 #fff);
  animation: l8 2s infinite alternate;
}
.loader:after {
  margin: 0 0 0 auto; 
  filter: drop-shadow(-40px 40px #fff);
  animation-delay: -1s;
}
@keyframes l8 {
  0%,10%   {border-radius:0}
  30%,40%  {border-radius:50% 0}
  60%,70%  {border-radius:50%}
  90%,100% {border-radius:0 50%}
}
</style>