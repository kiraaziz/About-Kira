<script>

    import allFramework from "./../../public/data/farmework.json"

    let indexType = 0

    let types = ["Frontend", "Backend", "Mobile", "language"]

</script>


<div class="h-max w-full flex items-center justify-start p-4 flex-col" id="Stack">
    <h1 class="text-4xl mt-4 font-bold shadow-xl px-3 py-1 text-white bg-gradient-to-tr from-blue-600 to-red-600 ">My Stack</h1>
    <div class="w-full h-full my-6 flex items-center justify-start flex-col lg:p-10" id="Stack">
        <div class="taps lg:m-5">
            {#each types as type , index}
                <button on:click={()=>{indexType = -5 ; indexType = index  }} class={`tab tab-xs lg:tab-lg text-white text-md tab-bordered lg:text-lg font-medium ${indexType === index && "tab-active"}`}>{type}</button>
            {/each}
        </div>
        <div  class="w-full grid lg:grid-cols-2 lg:grid-cols-1 lg:gap-2 px-5 lg:px-1 py-3">
            {#each allFramework as val}
                {#if val.type === indexType}
                    <div class="bg-gray-800/50 ease-in-out transition duration-100 hover:shadow-xl hover:bg-primary/50 hover:scale-105 hover:-translate-y-1 col-span-1 h-max border-4 rounded-xl border-white lg:p-5 p-3 flex items-center justify-center flex-col">
                        <img class="h-40 w-40 mb-4" alt="" src={`/icons/framework/${val.name}.svg`} />
                        <h1 class="text-xl font-bold text-white">{val.name}</h1>
    
                    </div>
                {/if}
            {/each}
        </div>
    </div>
    
</div>
