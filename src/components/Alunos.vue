<template>
  <div>
    <h1>{{titulo}}</h1>
    <input type="text" placeholder="Nome do Aluno" v-model="nome" v-on:keyup.enter="addAluno()">
    <button class="btn btn-Input" @click="addAluno(aluno)">Adicionar</button>
    <br>
    <table>
        <th>Mat.</th>
        <th>Nome</th>
        <th>Opções</th>
      <tbody>
        <tr v-for="(aluno, index) in alunos" :key="index">
          <td>{{index+1}}</td>
          <td>{{aluno.nome}}</td>
          <td>
            <button class="btn btn-Danger" @click="remover(aluno)">Remover</button>
          </td>
        </tr>
      </tbody>
    </table>

    
  </div>
</template>

<script>
export default {
  data() {
    return{
      titulo: 'Aluno',
    nome: "",
      alunos: [
      {id: 1, nome: 'Juliana'}, 
      {id: 2, nome: 'Maurílio'}, 
      {id: 3, nome: 'Isaias'}
      ]
    }
  },
  props: {
  },
  methods: {
    addAluno() {
      let _aluno = {
        nome: this.nome
      }
      this.alunos.push(_aluno);
      this.nome = '';
    },
    remover(aluno){
      let indice = this.alunos.indexOf(aluno);
      console.log(indice);
      this.alunos.splice(indice, 1);
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
input{
  border: 0;
  padding: 20px;
  font-size: 1.3em;
  color: #587f7f;
  display: inline;
}

.btn-Input{
  width: 150px;
  border: 0px;
  padding: 20px;
  font-size: 1.3rem;
  display: inline;
  background-color: rgb(116, 115, 115);
}

.btn-Input:hover{
  padding: 20px;
  margin: 0px;
  border: 0px;
}
</style>
