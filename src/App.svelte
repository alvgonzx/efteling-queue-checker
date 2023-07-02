<script>
  import Card from './lib/Card.svelte';
</script>

<main>
  <h1 class="text-3xl text-center font-bold pt-2">Efteling Queue Checker</h1>
		<div class="py-6 flex flex-col gap-4 w-full flex-nowrap md:flex-wrap md:flex-row">
      <Card name="Baron 1898" queue="70"></Card>
      <Card name="Baron 1898" queue="20"></Card>
      <Card name="Baron 1898" queue="10"></Card>
      <Card name="Baron 1898" queue="30"></Card>
      <Card name="Baron 1898" queue="60"></Card>
      <Card name="Baron 1898" queue="40"></Card>
    </div>
</main>