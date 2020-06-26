<template>
  
</template>

<script>
export default {
    name: 'LatestMovie',
    data(){
        return {
            wholeResponse: [],
            loading: true
        }
    },
    mounted(){
        fetch('https://api.themoviedb.org/3/movie/550?api_key=a0f264b76b8661bd95dab224d89a6504',
        {
            
            method: "GET",
            body: JSON.stringify(data),
            headers: {
                "Content-Type": "application/json"
            },
            credentials: "same-origin"
            }
         )
         .then(response => {
             this.wholeResponse = response.data.Search
         })
         .catch(error => {
             console.log(error)
         })
    }

}
</script>

<style lang="stylus" scoped>
    .v-progress-circular
        margin: 1 rem
</style>