<template>
    <form @submit.prevent="submitForm" class="user-form">
        <label>Имя</label>
        <input type="text" v-model="name" class="user-input"/>
        <label>Фамилия</label>
        <input type="text" v-model="surname" class="user-input"/>
        <label>Хобби</label>
        <input type="text" v-model="hobby" class="user-input"/>
        <label>Языки</label>
        <input type="text" v-model="langs" class="user-input"/>
        <button type="submit" class="submit-button">Отправить</button>
    </form>
</template>

<script>
export default{
    data(){
        return {
            name: '',
            surname: '',
            hobby: '',
            langs: ''
        }
    },
    methods: {
        submitForm(){
            this.$emit('form-submit', {
                name: this.name,
                surname: this.surname,
                hobby: this.hobby,
                langs: this.langs
            })
            this.name = ''
            this.surname = ''
            this.hobby = ''
            this.langs = ''
        }
    },
    name: "userForm"
}
</script>

<style scoped>
.user-form {
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 5px;
    background-color: #f9f9f9;
}

.user-form label {
    display: block;
    margin-bottom: 5px;
}

.user-input {
    width: 100%;
    padding: 8px;
    margin-bottom: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
}

.submit-button {
    padding: 10px 20px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

.submit-button:hover {
    background-color: #45a049;
}
</style>
