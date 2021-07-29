<template>
    <div class="container mt-5">
        <h1>Rentrez des choses à faire</h1>
        <form>
            <div class="form-group">
                <label for="action">Ton action :</label>
                <input v-model.lazy="formData.action" type="text" id="action" class="form-control">
                <button class="btn-primary mt-2" @click.prevent="addAction">Crée une tache</button>
            </div>
        </form>
        <br>
        <ul>
            <li class="card my-2" v-for="(action,index) in actions" v-bind:key="action.id">
                <div>
                    <p>{{ action }}</p>
                    <button class="btn btn-danger cross" @click="removeAction(index)">X</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>

export default {
    name: 'first',
    data() {
        return {
            submit: false,
            actions: [],
            formData: {
                action: '',
            }
        }
    },
    methods: {
        sendForm: function() {
            this.submit = true;
        },
        addAction: function() {
            if (this.formData.action.length > 0) {
                this.actions.push(this.formData.action);
                this.formData.action = '';
            }
        },
        removeAction: function(index) {
            console.log(index);
            this.actions.splice(index, 1);
        },
    },
}
</script>

<style>

p {
    padding: 10px;
}

.cross {
    position: absolute;
    top: 16px;
    right: 16px;
}

</style>
