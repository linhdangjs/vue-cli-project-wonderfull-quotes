<template>
    <div class="row">
        <form>
            <div class="col-sm-8 col-12 col-md-6 m-auto col-md-offset-3 form-group">
                <label for="">Quote</label>
                <textarea class="form-control" rows="3" cols="600" v-model="quote"></textarea>
            </div>
            <div class="col-sm-8 mt-3 mx-auto col-12 col-md-6 col-md-offset-3 form-group">
               <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
            </div>
        </form>
    </div>
</template>

<script>
    import Quote from "./Quote.vue"
    export default {
        data: function() {
            return {
                quote: ''
            }
        },
        methods: {
            createNew() {
                this.$emit('quoteAdded', this.quote);
                this.quote = '';
            }
        }
    }
</script>

<style>

</style>
