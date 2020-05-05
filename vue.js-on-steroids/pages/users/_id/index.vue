<template>
    <h1>Single user, with ID {{ $route.params.id }}</h1>
    <!-- $route gives us information about currently loaded route --> 
</template>

<script>
export default {
    validate(data) {
        // return data.params.id == 1
        return /^\d+$/.test(data.params.id) // checks if ID = to number
    }
}
</script>