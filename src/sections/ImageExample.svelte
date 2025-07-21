<script>
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";
</script>

<div>
    <Scroller layout="right">
        {#snippet sticky()}
            <img class="us-news-data" src="USNEWS.png" alt="US News Data on 20-year average tuition growth among national universities" />
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                <strong>
                    Your final project might look totally different from this
                    template!
                </strong>
            </ArticleText>

            <ArticleText>It's yours to create.</ArticleText>
        {/snippet}
    </Scroller>
</div>

<style>
    .us-news-data {
        width: 95%;
        margin: 0px auto;
    }
</style>
