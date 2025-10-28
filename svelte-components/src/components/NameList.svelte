<script>
    const names = [
        {
            firstName: 'Mr.DCT',
            lastName: 'Verla'
        },
         {
            firstName: 'Ngu',
            lastName: 'Rejoice'
        },
         {
            firstName: 'God',
            lastName: 'Jesus'
        },
    ]
</script>

<main>
    {#each names as name (name)}
      <slot name="hero" firstName={name.firstName} lastName={name.lastName} />
    {/each}
</main>