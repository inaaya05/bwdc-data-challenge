<script>
    let { children } = $props();
</script>

<div class="article-text">
    <p>
        {@render children()}
    </p>
</div>

<style>
    .article-text {
        margin: 15vh auto;
        width: 50%;
        background-color: #BBE6E4;
        color: #084B83;
        border: solid #084B83 3px;
        border-radius: 20px;
        padding: 20px;
        box-shadow: 10px 10px #42BFDD;
        text-align:center;
    }
</style>
