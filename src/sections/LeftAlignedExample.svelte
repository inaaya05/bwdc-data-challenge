<script>
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";

    
</script>

<div>
    <Scroller layout="left">
        {#snippet sticky()}
            <img class = "edu" src="Sheets_BWDC.png" alt="BWDC Undergrad Enrollment Rates By Race">
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                To the right, is a chart from the <a href="https://blackwealthdata.org/explore/education">BWDC</a>, displaying Undergraduate Enrollment Rates by Race/Ethnicity across the United States.
            </ArticleText>

            <ArticleText>
                It may be surprising to some, but the data clearly shows that enrollment rates have gone down over time across all races in the US.
            </ArticleText>

            <ArticleText>
                This information only highlights how important it is to make education more accessible and break down the barriers that deter many from pursuing it.
            </ArticleText>

            <ArticleText>
                When you consider the enrollment rates in the context of the cost of tuition over the years, the reasoning is almost self-explanatory...
            </ArticleText>
        {/snippet}
    </Scroller>
</div>

<style>
    .edu{
        width:95%;
        margin:0px auto;
    }
</style>
