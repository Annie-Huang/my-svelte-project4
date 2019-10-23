<script>
    let bro = 'Bro';

    function clickEvent() {
        bro = 'Dude';
    }

    let person = {
        status: 'woah'
    };

    let persons = [
        {status: 'dude', tagline: 'Yo sup'},
        {status: 'bro', tagline: 'Gnarly, man'},
        {status: 'chick', tagline: 'Watchoo want boo?'},
    ];

    let name = 'broseph';

    let status = false;
</script>

<h1>{bro}</h1>

<button on:click={clickEvent}>Click me</button>

{#if person.status == 'dude'}
    <h1>Dude!</h1>
{:else if person.status == 'bro'}
    <h1>bro!!</h1>
{:else}
    <h1>{person.status}</h1>
{/if}

<ul>
    {#each persons as {status, tagline}, i}
        <li>{i+1}: <strong>{status} </strong>({tagline})</li>
    {/each}
</ul>

<h1>{name}</h1>
<input bind:value={name}/>

<br />
<br />
<br />

<label>
    <input type="checkbox" bind:checked={status}/>
    Do you want to learn more svelte?
</label>

{#if status}
    <p>Of course I want to learn more</p>
{:else}
    <p>Nah, I just want to keep being a noob</p>
{/if}
