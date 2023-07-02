<script>
	export let name, queue, status;
</script>

<div class="md:w-1/4 block max-w-sm mx-auto  w-3/4 p-6 bg-white border border-gray-200 rounded-lg shadow hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700">
    <h5 class="mb-2 text-center text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{name}</h5>

    {#if queue > 30}
        <div class="w-full flex justify-center">
            <div class="text-xs mr-2 inline-flex items-center font-bold leading-sm uppercase px-3 py-1 bg-red-200 text-red-700 rounded-full">
                {queue} min
            </div>
            {#if status == false}
                <div class="text-xs inline-flex items-center font-bold leading-sm uppercase px-3 py-1 bg-red-200 text-red-700 rounded-full">
                    Closed
                </div>
            {:else}
                <div class="text-xs inline-flex items-center font-bold leading-sm uppercase px-3 py-1 bg-green-200 text-green-700 rounded-full">
                    Open
                </div>
            {/if}
        </div>
    {:else if queue == 30}
        <div class="w-full flex justify-center">
            <div class="text-xs mr-2 inline-flex items-center font-bold leading-sm uppercase px-3 py-1 bg-orange-200 text-orange-700 rounded-full">
                {queue} min
            </div>
        
            {#if status == false}
                <div class="text-xs inline-flex items-center font-bold leading-sm uppercase px-3 py-1 bg-red-200 text-red-700 rounded-full">
                    Closed
                </div>
            {:else}
                <div class="text-xs inline-flex items-center font-bold leading-sm uppercase px-3 py-1 bg-green-200 text-green-700 rounded-full">
                    Open
                </div>
            {/if}
        </div>
    {:else}
        <div class="w-full flex justify-center">
            <div class="text-xs mr-2 inline-flex items-center font-bold leading-sm uppercase px-3 py-1 bg-green-200 text-green-700 rounded-full">
                {queue} min
            </div>
            {#if status == false}
                <div class="text-xs inline-flex items-center font-bold leading-sm uppercase px-3 py-1 bg-red-200 text-red-700 rounded-full">
                    Closed
                </div>
            {:else}
                <div class="text-xs inline-flex items-center font-bold leading-sm uppercase px-3 py-1 bg-green-200 text-green-700 rounded-full">
                    Open
                </div>
            {/if}
        </div>
    {/if}
</div>
