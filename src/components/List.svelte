<script>
    let people = [
        { name: 'juno', hairColor: 'brown', age: 25, id: 1 },
        { name: 'mario', hairColor: 'black', age: 45, id: 2 },
        { name: 'lily', hairColor: 'pink', age: 35, id: 3 },
    ];
</script>

<div>
    {#each people as person, index (person.id)}
        <div>
        <h4>{index + 1} {person.name}</h4>
        <p>{person.age} years old, {person.hairColor} hair</p>
        </div>
        {:else}
        <p>There are no people to show...</p>
    {/each}
</div>