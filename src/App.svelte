<script>
  import Leaderboard from "./Leaderboard.svelte";
  let leaderboards = [
    {
      name: "Work from office",
      id: 0,
      players: [
        {
          name: "Ferraaaaaaaaaaaaaaaaaaaaaafsasdfasdfsdaan",
          strike: 10,
          id: 0,
        },
        { name: "Joan", strike: 9, id: 1 },
        { name: "Seve", strike: 11, id: 2 },
        { name: "Irene", strike: 12, id: 3 },
        { name: "Aitor", strike: 0, id: 4 },
        { name: "Javi", strike: 3, id: 5 },
        { name: "Adrián", strike: 2, id: 6 },
      ],
    },

    {
      name: "No croissant",
      id: 1,
      players: [
        { name: "Ferran", strike: 10, id: 0 },
        { name: "Joan", strike: 0, id: 1 },
        { name: "Jorge", strike: 14, id: 7 },
      ],
    },
  ];
</script>

<main>
  <h1>FitLifeBSC</h1>
  {#each leaderboards as leaderboard (leaderboard.id)}
    <Leaderboard {...leaderboard} />
  {/each}
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: blue;
    font-size: 4em;
  }

  @media (min-width: 0px) {
    main {
      max-width: none;
    }
  }
</style>
