<script>
    export default {
        // Add code if/as necessary
        // Hint: Add properties subject, entry and mood
        props: {
            subject: String,
            entry: String,
            mood: String
        },
        computed: {
            imgLoc() {
                return `/assets/${this.mood.toLowerCase()}.png`
            }
        }
    }
</script>


<template>
    <!-- TODO: add your template code here. Use boostrap card -->
    <div class="card" style="width:18em">
        <img class="card-img-top" :src="imgLoc"></img>
        <div class="card-body">
            <h4 class="card-title">{{ subject }}</h4>
            <p class="card-text">{{ entry }}</p>
            <hr/>
            <a class="btn btn-danger" href="">Delete</a>
        </div>
    </div>
    <br/>
</template>

