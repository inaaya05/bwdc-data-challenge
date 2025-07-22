<script>
    import Scroller from "../lib/Scroller.svelte";
    import ObservedArticleText from "../lib/ObservedArticleText.svelte";

    // this `options` object below is passed into the <ObservedArticleText>
    // component, and from there it gets passed to the IntersectionObserver object w
    // when it's created.
    // the thresholds to fire the callback are 85% and 95%. in the callback function,
    // we check whether the visible area is >= 90%. so, triggering the callback at
    // 85% and 95% ensures we trigger the correct change in background color
    // whether the element is being scrolled into the viewport or out of the viewport.
    const options = {
        threshold: [0.85, 0.95],
    };

    const callback = (entries, observer) => {
        entries.forEach((entry) => {
            const elem = entry.target;

            if (entry.intersectionRatio >= 0.9) {
                // "active" state
                elem.style.backgroundColor = "#BBE6E4";
            } else if (entry.intersectionRatio < 0.9) {
                // "inactive" state
                elem.style.backgroundColor = "#42BFDD";
            }
        });
    };
</script>

<div>
    <Scroller layout="left">
        {#snippet sticky()}
            <div>
                <img class="action" src="action.png" alt="People with shirts of different shades of blue holding each other with their backs facing the viewer.">
            </div>
        {/snippet}

        {#snippet scrolly()}
            <ObservedArticleText {callback} {options}>
                <code>{""}</code> <strong>Check out these resources:</strong>
            </ObservedArticleText>

            <ObservedArticleText {callback} {options}>
                <code>{""}</code> <a href="https://www.collegeessayguy.com/blog/pay-for-college-crash-course">Look into how YOU can afford college!</a>
            </ObservedArticleText>

            <ObservedArticleText {callback} {options}>
                <code>{""}</code> <a href="https://www.msudenver.edu/10-benefits-of-higher-education/">Discover the importance of higher education!</a>
            </ObservedArticleText>

            <ObservedArticleText {callback} {options}>
                <code>{""}</code> <a href="https://vote.gov/guide-to-voting">Understand how to vote in favor of accessible education!</a>
            </ObservedArticleText>
        {/snippet}
    </Scroller>
</div>
<style>
    .action{
        width:95%;
        margin:0px auto;
    }
</style>