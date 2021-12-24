<template>
    <div class="container">
         <form @submit.prevent="enviarFormulario"><!--@submit tratar o submite e o prevent interrope o comportamento padrão que efetura o recarregamento da pagina  -->
            <div class="form-group">
                <label for="nome">Nome</label>
                <input type="text" class="form-control" id="nome" v-model="usuario.nome">
            </div>
            <div class="form-group">
                <label for="email">E-mail</label>
                <input type="email" class="form-control" id="email" v-model="usuario.email">
            </div>
            <div class="form-group">
                <label for="senha">Senha</label>
                <input type="password" class="form-control" id="nome" v-model="usuario.senha">
            </div> 
            <button class="btn btn-primary" type="submit">Salvar</button>
        </form>
    </div>
</template>

<script>
export default {

    data: function () {//data é um objeto que vai ser passado para o componente
        return {
            usuario: {
                nome: '',
                email: '',
                senha: ''
            }
        }
    },
    methods: {
        enviarFormulario () {
            console.log(this.usuario);
        }
    }
}
</script>

<style>

</style>