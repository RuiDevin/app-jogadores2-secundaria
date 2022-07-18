<script>
import { v4 as uuid } from "uuid";
export default {
  data() {
    return {
      novo_time: "",
      jogadores: [
        { id: 1, name: "Jogador 1" },
        { id: 2, name: "Jogador 2" },
        { id: 3, name: "Jogador 3" },
        { id: 4, name: "Jogador 4" },
      ],
    };
  },
  methods: {
    salvar() {
      const novo_id = uuid();
      this.jogadores.push({
        id: novo_id,
        name: this.novo_jogador,
      });
    },
    excluir(jogador) {
      const indice = this.jogador.indexOf(jogador);
      this.times.splice(indice, 1);
    },
  },
};
</script>

<template>
  <div class="container">
    <h2>Gerenciamento de jogadores</h2>
  </div>
  <div class="form-input">
    <input type="text" v-model="novo_jogador" placeholder="Jogador" />
    <button @click="salvar">Salvar</button>
  </div>
  <div>
    <div class="list-times">
      <table>
        <thead>
          <tr>
            <th>ID</th>
            <th>Nome</th>
            <th>Açoẽs</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="jogador in jogadores" :key="jogador.id">
            <td>{{ jogador.id }}</td>
            <td>{{ jogador.name }}</td>
            <td><button @click="excluir(jogador)">excluir</button></td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<style scoped>
.form-input {
  cursor: pointer;
}
</style>
