<script>
import { v4 as uuid } from "uuid";
import {axios} from 'axios';

export default {
  data() {
    return {
      novo_time: "",
      times: [
        { id: "ab0b59c9-c846-4349-904f-ba5d1cf53329", name: "Time 1" },
        { id: "1262e7a2-6ba2-405a-8ca6-044a3406afd0", name: "Time 2" },
        { id: "f5df0e90-d169-4f4f-aae3-721c03e03e59", name: "Time 3" },
        { id: "b5f66fe8-a9fc-4eb6-a26f-f690ff0512df", name: "Time 4" },
      ],
    };
  },
  methods: {
    salvar() {
      const novo_id = uuid();
      this.times.push({
        id: novo_id,
        name: this.novo_time,
      });
    },
    excluir(time) {
      const indice = this.times.indexOf(time);
      this.times.splice(indice, 1);
    },
  },
};
</script>

<template>
  <div class="container">
    <h2>Gerenciamento de time</h2>

    <div class="form-input">
      <input type="text" v-model="novo_time" placeholder="Time" />
      <button @click="salvar">Salvar</button>
    </div>
    {{ times }}
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
          <tr v-for="time in times" :key="time.id">
            <td>{{ time.id }}</td>
            <td>{{ time.name }}</td>
            <td>???</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
