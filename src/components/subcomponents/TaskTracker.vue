<script>
    // TODO: Complete the code
    export default { 
        data() {
            return {
                
            }
        },
        // Hint: insert properties task (Object) and idx (Number)
        props: {
            task: Object,
            idx: Number
            
        },
        emits: [
            'removeTask'
        ]
    }
</script>

<template>
    <!-- TODO: add your template code here --> 
    <div class="card" style="width:18em; display: inline-block;">
        <div class="card-body">
            <h4 class="card-title">Deadline: {{ task.deadline }}</h4>
            <p class="card-text">{{ task.desc }}</p>
            <hr/>
            <button class="btn btn-danger" @click="$emit('removeTask', idx)">Done</button>
        </div>
    </div>
    <br/>
</template>
