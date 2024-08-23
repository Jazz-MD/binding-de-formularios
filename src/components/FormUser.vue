<script>
export default {
  name: 'FormUser',
  data() {
    return {
      user: {
        titulo: '',
        chip: '',
        numero: '',
        fecha: '',
        propietario: '',
        tipo: ''
      }
    }
  }
}
</script>
<template>
  <form>
    <div>
      <label for="user-titulo" class="form-label">Título de la tarjeta:</label>
      <input id="user-titulo" class="form-control" type="text" v-model="user.titulo" />
    </div>

    <div>
      <label>Chip SRC: </label>
      <input v-model="user.chip" />
    </div>

    <div>
      <label for="user-numero" class="form-label">Número:</label>
      <input id="user-numero" class="form-control" type="text" v-model="user.numero" />
    </div>

    <div>
      <label for="user-fecha" class="form-label">Fecha de expiración:</label>
      <input id="user-fecha" class="form-control" type="text" v-model="user.fecha" />
    </div>

    <div>
      <label for="user-propietario" class="form-label">Propietario:</label>
      <input id="user-propietario" class="form-control" type="text" v-model="user.propietario" />
    </div>

    <div>
      <label for="user-tipo" class="form-label">Tipo de tarjeta SCR:</label>
      <input v-model="user.tipo" />
    </div>
  </form>
  <div class="carnet">
    <h3>{{ user.titulo }}</h3>
    <img width="40" :src="user.chip" alt="chip" />
    <div>
      <h2>{{ user.numero }}</h2>
      <span
        >Fecha Exp: <b>{{ user.fecha }}</b></span
      >
    </div>
    <footer>
      <span>{{ user.propietario }}</span>
      <img :src="user.tipo" width="60" alt="Visa" />
    </footer>
  </div>
</template>
<style scoped>
form {
  padding: 18px;
  border-radius: 20px;
  border: ridge 1px;
  box-shadow: 1px 1px 1px 1px gray;
  font-weight: bold;
  display: flex;
  flex-direction: column;
  gap: 15px;
  justify-content: center;
  background: #1c1a1e;
  color: white;
}
form div {
  display: grid;
  grid-template-columns: 100px 200px;
  align-items: center;
  gap: 5px;
}

form div label {
  text-align: right;
}

.carnet {
  width: 400px;
  height: 230px;

  background-color: #00dbde;
  background-image: linear-gradient(90deg, #00dbde 0%, #fc00ff 100%);

  color: white;
  border-radius: 20px;
  padding: 20px;
  box-shadow: 0px 0px 10px 2px black;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

h3 {
  font-size: 20px;
}

h2 {
  font-size: 30px;
  letter-spacing: 10px;
  margin-bottom: 15px;
  text-shadow: 0px 0px 1px gold;
  font-family: Times;
}

b {
  font-size: 16px;
}

footer {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;
  font-weight: bold;
  font-size: 18px;
  text-transform: uppercase;
  font-style: italic;
}
</style>
