<template>
    <div class="user-data">
        <p>Введенная вами информация</p>
        <p>Имя: {{ userData.name }}</p>
        <p>Фамилия: {{ userData.surname }}</p>
        <p>Хобби: {{ userData.hobby }}</p>
        <p>Языки: {{ userData.langs }}</p>
    </div>
</template>

<script>
export default {
    props: {
        userData: {
            type: Object,
            required: true
        }
    },
    name: "userData"
}
</script>

<style scoped>
.user-data {
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 5px;
    background-color: #f9f9f9;
}

.user-data p {
    margin-bottom: 10px;
}

.user-data p:last-child {
    margin-bottom: 0;
}
</style>
