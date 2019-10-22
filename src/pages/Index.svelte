<script>
    let bro = 'Bro';

    function clickEvent() {
        bro = 'Dude';
    }
</script>

<h1>{bro}</h1>

<button on:click={clickEvent}>Click me</button>
