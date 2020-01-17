<script>
    export let href;
    export let icon;
    export let alt;
</script>
<style>
    .icon {
        height: 100%;
        width: auto;
        margin-left: 3rem;
        margin-right: 3rem;
    }
</style>

<a href={href} target="_blank" rel="noreferrer noopener">
    <img class="icon" src={icon} alt={alt} />
</a>