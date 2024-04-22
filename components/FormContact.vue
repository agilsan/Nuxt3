<template>
    <form>
        <div class="mb-3">
            <label for="inputName" class="form-label">Name</label>
            <input type="email" class="form-control" id="inputName" aria-describedby="nameHelp">
        </div>
        <div class="mb-3">
            <label for="inputEmail" class="form-label">Email address</label>
            <input type="email" class="form-control" id="inputEmail" aria-describedby="emailHelp">
        </div>
        <div class="mb-3">
            <label for="formControlTextarea" class="form-label">Message</label>
            <textarea class="form-control" id="formControlTextarea" rows="3"></textarea>
        </div>
        <button type="submit" class="btn btn-primary">Submit</button>
    </form>
</template>

<script setup>

</script>

<style>

</style>