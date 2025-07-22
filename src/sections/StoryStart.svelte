<script>
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";

    
</script>

<div>
    <Scroller layout="left">
        {#snippet sticky()}
            <img class = "girl" src="girlschool.jpg" alt="Young girl who is ready to take on her education!">
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                Meet Sara...
            </ArticleText>

            <ArticleText>
                A girl from the suburbs of Michigan, who lives a relatively normal life.
            </ArticleText>

            <ArticleText>
                She has hopes and dreams of growing up and achieving something wonderful in her life. She's not sure if that would be as a doctor, teacher, astronaut, or engineer. But she definitely wants to keep her education going.
            </ArticleText>

            <ArticleText>
                In the twelfth grade, she received a full ride to a college a little further from home.
            </ArticleText>

            <ArticleText>
                She was so excited! She knew that her parents didn't have the means to take on four years of tuition, and being fresh out of high school, she definitely did not either.
            </ArticleText>

            <ArticleText>
                However, it was not that simple for Sara. Her family may not have had the money for school, but they refused to let her move out.
            </ArticleText>

            <ArticleText>
                "It's not proper."
            </ArticleText>

            <ArticleText>
                Here she was, attending a college five minutes from home, excited to start her educational journey despite the fear of financial ruin looming at the back of her mind...
            </ArticleText>

            <ArticleText>
                It wasn't until she started college that she realized, for her parents, college was just a prerequisite to marriage, and that was why they valued keeping her at home.
            </ArticleText>

            <ArticleText>
                Now, Sara is passionate about making education more accessible so that she can continue her own and build her career without worry about cultural/social pressure or financial barriers that may try to hold her back.
            </ArticleText>

            <ArticleText>
                She believes that even if the cards are stacked against her, she can shuffle the deck and take control of her own story.
            </ArticleText>
        {/snippet}
    </Scroller>
</div>

<style>
    .girl{
        width:90%;
        margin:0px auto;
    }
</style>
