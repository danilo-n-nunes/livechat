<template>
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-md-8">
                <div class="card">
                    <div class="card-header">Estudando Vue</div>

                    <div class="card-body">
                        <input type="text" v-model="text">
                        {{text}}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data: () => {
            return {
                text: ''
            }
        },
        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
