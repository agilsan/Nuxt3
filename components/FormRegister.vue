<template>
    <form>
        <div class="mb-3">
            <label for="inputUserName" class="form-label">Username</label>
            <input type="email" class="form-control" id="inputUserName" aria-describedby="emailHelp">
        </div>
        <div class="mb-3">
            <label for="inputEmail1" class="form-label">Email address</label>
            <input type="email" class="form-control" id="inputEmail1" aria-describedby="emailHelp">
            <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
        </div>
        <div class="mb-3">
            <label for="inputPassword1" class="form-label">Password</label>
            <input type="password" class="form-control" id="inputPassword1">
        </div>
        <div class="mb-3">
            <label for="inputPassword2" class="form-label">Re-Password</label>
            <input type="password2" class="form-control" id="inputPassword2">
        </div>
        <button type="submit" class="btn btn-primary">Submit</button>
    </form>
</template>

<script setup>

</script>

<style>

</style>