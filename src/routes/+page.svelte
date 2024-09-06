<script>
    /** @type {import('./$types').PageData} */
   export let data 
</script>

<main>
    <picture>
        <img src="{data.person.avatar}" alt="profiel foto">
    </picture>

    <section>
        <h1>
            A problem had been detected and Windows has
            been shut down to prevent damage to
            your computer.
        </h1>

        <h2>UNMOUTABLE_BOOT_VOLUME</h2>

        <p>
            We’ve detected an error called: ”{data.person.name.toUpperCase()}-{data.person.surname.toUpperCase()}.EXE”, also known as: “{data.person.nickname}”.
            If this is the first time you’ve seen this error, restart your computer.
            If this screen appears again, you should seek help at: <a href="{data.person.website}">https://github.com/</a>.
            
            If you want to know about this issue, seek help bij looking through information
            noted as: “{data.person.github_handle}”. 
        </p>

        <h2>{data.person.name.toUpperCase()}-MESSAGE_ERROR_205</h2>
        <p>"{data.person.bio}"</p>
    </section>
</main>

<style>
    @font-face {
    font-family: "Pixel";
    src:
        url("assets/font/Jersey20-Regular.ttf");
    }

    :root {
        background-color: blue;
    }

    main {
        font-family: "Pixel", sans-serif;
        color: white;
        letter-spacing: .04em;
        width: 70%;
    }

    h1,
    h2 {
        --h1-size: 3em;
        --h2-size: 2em;

        font-weight: 500;
    }

    h1 {
        font-size: var(--h1-size);
    }

    h2 {
        font-size: var(--h2-size);
    }

    p {
        --p-size: 1.4em;
        font-size: var(--p-size);
        line-height: 1.2em;
        font-weight: 300;
    }
</style>