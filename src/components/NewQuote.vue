<template>
    <form class="">
        <div class="row form-group justify-content-center ">
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 
                        col-md-8 col-md-offset-2"
            >
                <label for="newQuote">Quote</label>
                <textarea name="newQuote" rows="3"
                          class="form-control"
                          v-model="quote"
                >

                </textarea>
            </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 
                        col-md-8 col-md-offset-2"
            >
                <button class="btn btn-primary" @click.prevent="createNew">Add quote</button>
            </div>
        </div>
    </form>
</template>

<script>
export default {
    data() {
        return {
            quote: ''
        }
    },
    methods: {
        createNew() {
            this.$emit('quoteAdded', this.quote)
            this.quote = ''
        }
    },
}
</script>

<style lang="css">
    
</style>