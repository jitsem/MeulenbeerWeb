<template>
    <div>
        <h3>{{beer.title}}</h3>
        <p>{{beer.description}}</p>
    </div>
</template>

<script>
export default {
    name: 'Beer',
    props: ["beer"],
}
</script>