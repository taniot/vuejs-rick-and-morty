<script>
import { store } from '../store';
export default {
    name: 'Search',
    data() {
        return {
            store
        }
    },
    methods: {
        // testSubmit(){
        //     console.log('modulo inviato');
        //     console.log(this.store.searchKey);
        // }
    }
}
</script>

<template>
    <div class="container">
        <form @submit.prevent="$emit('pippo')">
            <div class="row justify-content-center g-1">
            <div class="mb-3 col-12 col-sm-auto">
                <label for="search-character" class="form-label d-none">Search Character</label>
                <input type="text" class="form-control" id="search-character" placeholder="Search Character" v-model="store.searchKey">
            </div>
            <div class="mb-3 col-12 col-sm-auto">
                <label for="search-status" class="form-label d-none">Select Status</label>
                <select class="form-select" id="search-status" v-model="store.searchStatus">
                    <option selected value="">Select Status</option>
                    <option>alive</option>
                    <option>dead</option>
                    <option>unknown</option>
                </select>
            </div>
            <div class="mb-3 col-12 col-sm-auto">
                <button type="submit" class="btn btn-primary me-1">Search</button>
                <button type="reset" class="btn btn-secondary">Reset</button>
            </div>
        </div>
        </form>
    </div>
</template>

<style lang="scss" scoped></style>