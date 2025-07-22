<script>
    let { title, subtitle} = $props();
</script>

<div class="title-card">
    <div class="content">
        <h1>{title}</h1>
        <p>{subtitle}</p>
    </div>
</div>

<style>
    .title-card {
        background-color: #bbe6e4;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 2rem;
        box-sizing: border-box;
        font-family: "Inter", sans-serif;
    }

    .content {
        max-width: 700px;
        background-color: #bbe6e4;
        padding: 2rem;
        border: 6px solid #084b83;
        border-radius: 2rem;
        box-shadow: 16px 16px #42bfdd;
    }

    h1 {
        font-size: 3rem;
        margin: 0;
        color: #084B83;
        text-shadow: 1px 1px 0 #42bfdd;
    }

    p {
        font-size: 1.3rem;
        color: #084B83;
        margin-top: 1rem;
    }

    @media (max-width: 600px) {
        h1 {
            font-size: 2.2rem;
        }

        p {
            font-size: 1.1rem;
        }
    }
</style>
