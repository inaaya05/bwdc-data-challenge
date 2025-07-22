<script>
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";
</script>

<div>
    <Scroller layout="right">
        {#snippet sticky()}
            <img class="us-news-data" src="sheets-usnews.png" alt="US News Data on 20-year average tuition growth among national universities" />
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                In this graph from <a href="https://www.usnews.com/education/best-colleges/paying-for-college/articles/see-20-years-of-tuition-growth-at-national-universities">US News</a> we can even see that as time has gone on, the cost of college tuition alone has increased significantly.
            </ArticleText>
            <ArticleText>In fact, tuition and fees at private, out-of-state public, and in-state public universities have risen 126%, 112%, and 133%, respectively.</ArticleText>
            <ArticleText>If these numbers are adjusted for inflation, they've risen 41% (private universities), 32% (out-of-state public universities), and 45% (in-state public universities).</ArticleText>
        {/snippet}
    </Scroller>
</div>

<style>
    .us-news-data {
        width: 95%;
        margin: 0px auto;
    }
</style>
