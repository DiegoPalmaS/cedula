<script>
  import bandera from './assets/chile_bandera.png'
  import elon from './assets/foto_elon.jpg'

  export default {
    name: 'App',
    data(){
      return {
        bandera,
        elon,
        firstname: 'ELON REEVE',
        lastname: 'MUSK',
        run: '22.222.222-2',
        country: 'SUDAFRICANO',
        gender: 'M',
        birthdate: '28 JUN 1971',
        documentNumber: '222.222.222',
        emissionDate: '01 ENE 2025',
        expirationDate: '01 ENE 2030',
      }
    }
  }
</script>

<template>
  <div class="carnet">
      <aside>
        <div>
          <span>CEDULA DE INDENTIDAD</span>
          <img width="40" :src='bandera' alt="bandera de chile" />
        </div>

        <img :src='elon' alt="fotografía de elon musk"/>
        <p>RUN {{run}}</p>
      </aside>

      <main>
        <header>
          <p>REPUBLICA DE CHILE</p>
          <span>SERVICIO DE REGISTRO CIVIL E IDENTIFICACIÓN</span>
        </header>
        <section>
          <article>
            <header>APELLIDOS</header>
            <span>{{lastname}}</span>
          </article>
          <article>
            <header>NOMBRES</header>
            <span>{{firstname}}</span>
          </article>

          <div class="grid-2-colums">
            <article>
              <header>NACIONALIDAD</header>
              <span>{{country}}</span>
            </article>
            <article>
              <header>SEXO</header>
              <span>{{gender}}</span>
            </article>
          </div>
          <div class="grid-2-colums">
            <article>
              <header>FECHA DE NACIMIENTO</header>
              <span>{{birthdate}}</span>
            </article>
            <article>
              <header>NÙMERO DOCUMENTO</header>
              <span>{{documentNumber}}</span>
            </article>
          </div>
          <div class="grid-2-colums">
            <article>
              <header>FECHA DE EMISIÒN</header>
              <span>{{emissionDate}}</span>
            </article>
            <article>
              <header>FECHA DE VENCIMIENTO</header>
              <span>{{expirationDate}}</span>
            </article>
          </div>
          <article>
            <header>FIRMA DEL TITULAR</header>
            <span>X Æ A-12</span>
          </article>
        </section>
      </main>
    </div>
</template>

<style>
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 60vh;
  font-size: 10px;
  font-family: sans-serif;
}

.carnet {
  width: 400px;
  height: 230px;
  background: #c8deed;
  border-radius: 20px;
  display: grid;
  grid-template-columns: 30% 1fr;
  padding: 15px;
  box-shadow: 0px 0px 10px 2px black;
}

aside div {
  display: flex;
}

aside > img {
  margin-top: 15px;
  width: 100%;
}

aside p {
  text-align: center;
  font-size: 12px;
  font-weight: bold;
}

main {
  padding: 0px 14px;
}

main article {
  margin: 4px 0px;
}

main article header {
  font-weight: bold;
  color: #0235a4;
  font-size: 8px;
}

main header p {
  font-size: 20px;
  margin: 0;
  font-weight: bold;
  color: #0235a4;
}

main header span {
  font-size: 8px;
  color: #399be1;
}

main section {
  margin-top: 10px;
}

main section article span {
  font-size: 13px;
  font-weight: 600;
}

main section .grid-2-colums {
  display: grid;
  grid-template-columns: 50% 50%;
}
</style>
