<script>
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";
</script>

<div id="right-align">
    <Scroller layout="right">
        {#snippet sticky()}
            <img class="blueshelf" href="blueshelf.jpg" alt="Blue book shelf"> 
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                Education in the US is a tricky pursuit.
            </ArticleText>

            <ArticleText>
                There are many barriers and obstacles to higher education...
            </ArticleText>

            <ArticleText>
                <strong>🚧Barrier🚧</strong>
                <br/><br/>
                <strong>Financial Means</strong>
                <br/><br/>
                We all know that college is expensive, but it's more than just tuition that costs money, books, housing, food, it all adds up. Without the means to pursue such a costly endeavor, it is difficult to even go for a degree.
            </ArticleText>

            <ArticleText>
                <strong>🚧Barrier🚧</strong>
                <br/><br/>
                <strong>Lack of Representation</strong>
                <br/><br/>
                There's more than just being able to pay for college, there's also the mental aspect of it all. Growing up, if you don't see others who look like you in fields that require lots of education, you may not feel like you belong in spaces that require lots of education. This discourages many from pursuing higher education.
            </ArticleText>
            <ArticleText>
                <strong>🚧Barrier🚧</strong>
                <br/><br/>
                <strong>Inadequate Preparation</strong>
                <br/><br/>
                Some things are especially out of our control. It's not always about making enough money in time to pay the tuition bill or reminding yourself that you can be the representation you wished you would've had in your field of choice, it might be that growing up, you were at a school that did not have the resources to prepare you for such rigorous academic work, and that can lead to failing out or losing any semblance of motivation to continue.
            </ArticleText>
        {/snippet}
    </Scroller>
</div>

<style>
    .blueshelf{
        width: 95%;
        margin: 0px auto;
    }
</style>
