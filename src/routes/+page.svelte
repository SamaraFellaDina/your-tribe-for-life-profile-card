<script>
   export let data 
</script>

<body>
    <main>
        <ul>
            <li>
                <picture>
                    <img src="{data.person.avatar}" alt="profiel foto">
                </picture>
            </li>
            <li>
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
            </li>
        </ul>
    </main>
</body>

<style>
    @font-face {
    font-family: "Pixel";
    src: url("/fonts/Jersey20-Regular.ttf");
    }

    :root {
        background-color: blue;
    }

    body {
        display: flex;
        justify-content: center; 
        align-items: center; 
        height: 100vh; 
        margin: 0;
    }
    
    main {
        --average-padding: 1em 0;
        font-family: "Pixel", sans-serif;
        color: white;
        letter-spacing: .04em;
        padding: var(--average-padding);
        width: 80%;
        margin: 0 auto;
        
        @media screen and (min-width: 1080px) {
            width: 50em;
        }

    }

    h1,
    h2,
    p  {
        --main-color: rgb(255, 255, 255);
        color: var(--main-color);
    }

    h1,
    h2 {
        --h1-size: 3em;
        --h2-size: 2em;
        line-height: .8em;
        font-weight: 500;
    }

    ul,
    li {
        display: block;
        list-style-type: none;
        margin-block-start: 0;
        margin-block-end: 0;
        margin-inline-start: 0px;
        margin-inline-end: 0px;
        padding-inline-start: 0px;
        unicode-bidi: isolate;
    }

    ul li:nth-child(1){
        display: flex;
        margin: 0 auto;
        justify-content: center;
    }

    img {
        --image-format: 8em;
        width: var(--image-format);
        height: var(--image-format);
    }

    h1 {
        --margin-block: 1em;
        margin-block-start: var(--margin-block);
        margin-block-end: var(--margin-block);
        font-size: var(--h1-size);
    }

    h2 {
        --margin-block:.3em;
        margin-block-start: var(--margin-block);
        margin-block-end: var(--margin-block);
        font-size: var(--h2-size);
    }

    p {
        --p-size: 1.4em;
        --margin-block:.3em;

        margin-block-start: var(--margin-block);
        margin-block-end: var(--margin-block);

        font-size: var(--p-size);
        line-height: 1.2em;
        font-weight: 300;
    }
    
    a {
        --hyperlinks: rgb(0, 255, 0);
        color: var(--hyperlinks);
    }
</style>