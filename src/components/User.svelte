<script>
    const path= "avatars"
    export let user
</script>

<img src="{path}/{user[1]}" alt="{user[0]}">

<style>
    img {
        max-width: 48px;
        max-height: 48px;
        border-radius: 33%;
    }
</style>
