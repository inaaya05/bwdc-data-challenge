<script>
    import { onMount } from "svelte";

    let { children, callback, options } = $props();

    // this uniqueId just lets us target the element 
    // with `document.getElementById(uniqueId)` later on.
    // it's a little hacky, but it works. 
    let uniqueId = Math.random().toString();

    // here we define the onMount() function for this component.
    // svelte handles calling the onMount() function *after* all of the HTML in this
    // component has been mounted to the DOM. we have to put the intersection observer
    // stuff in onMount() because we need to target the <div> we create below,
    // but it won't actually exist in the DOM until it's been mounted. 
    onMount(() => {
        let intersectionObserver = new IntersectionObserver(callback, options);

        const observedElement = document.getElementById(uniqueId);
        intersectionObserver.observe(observedElement);
    });
</script>

<!-- assign the containing div the id `uniqueId` so we can target it -->
<div id={uniqueId} class="article-text">
    <p>
        {@render children()}
    </p>
</div>

<style>
    .article-text {
        margin: 20vh auto;
        width: 50%;
        background-color: #BBE6E4;
        color: #084B83;
        border: solid #084B83 3px;
        border-radius: 10px;
        padding: 10px;
        box-shadow: 16px 16px #42BFDD;
        text-align:center;
    }
</style>
