<script>
  import { onMount } from 'svelte';
  import Card from './lib/Card.svelte';

  const proxy_url = 'https://corsproxy.io/?';
  const api_url = 'https://queue-times.com/parks/160/queue_times.json';

  let lands = [];

  const fetchRides = async () => {
    const response = await fetch(`${proxy_url}${api_url}`);
    const data = await response.json();

    lands = data.lands;
  }

  onMount(() => {
    fetchRides();
  })
</script>

<main>
  <h1 class="text-3xl text-center font-bold pt-2">Efteling Queue Checker</h1>
		<div class="py-6 flex flex-col gap-4 w-full flex-nowrap md:flex-wrap md:flex-row">
      {#each lands as land}
        {#each land.rides as ride}
          <Card name={ride.name} queue={ride.wait_time} status={ride.is_open ? true : false}/>
        {/each}
      {/each}
    </div>
</main>