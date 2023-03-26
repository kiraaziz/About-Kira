<script>
    import { each } from "svelte/internal";


    import projects from "../../public/data/projects.json"
//    

</script>
<div class="h-max w-full flex items-center justify-start p-4 flex-col" id="Projects">
    <h1 class="mb-10 text-4xl font-bold shadow-xl px-3 py-1 text-white bg-gradient-to-tr from-blue-600 to-red-600 ">My Projects</h1>
    <div class="w-full grid p-2 gap-2 lg:grid-cols-3 grid-cols-1">
        {#each projects as project , index}
            {#if index % 2 === 0 }
                <div class="lg:col-span-2 hidden lg:block border-4 border-white rounded-xl w-full h-full">
                    <img src={project.images[0]} class="w-full rounded-xl h-max w-max max-h-[80vh] object-cover mx-auto" />
                </div>
                <div class="bg-gray-800 col-span-1 rounded-xl lg:p-7 p-3 space-y-3 flex flex-col items-start justify-center  ">

                    <div class="carousel rounded-box">
                        {#each project.images as img }
                            <div class="carousel-item w-full">
                                <img src={img} class="w-full h-auto object-cover mb-5 rounded-xl lg:hidden block border-white border-4" alt="Burger" />
                            </div> 
                        {/each}
                    </div>
                    <h1 class="w-max bg-gray-900 border-l-4 px-2 border-primary text-lg font-bold text-primary">{project.name}</h1>
                    {#if project.url}
                        <a class="link link-primary" href={project.url}>{project.url}</a>
                    {/if}
                    <h1 class="font-light text-white">{project.description}</h1>
                    <div class="w-full h-max flex flex-wrap ">
                        {#each project.tags.split(" ") as tag}
                            <button class="bg-primary/50 m-1 px-3 py-1 rounded-full text-white font-medium">{tag}</button>
                        {/each}
                    </div>
                </div> 
            {:else}
                <div class="bg-gray-800 col-span-1 rounded-xl lg:p-7 p-3 space-y-3 flex flex-col items-start justify-center">
                
                    <div class="carousel rounded-box">
                        {#each project.images as img }
                            <div class="carousel-item w-full">
                                <img src={img} class="w-full h-auto object-cover mb-5 rounded-xl lg:hidden block border-white border-4" alt="Burger" />
                            </div> 
                        {/each}
                    </div>
                    <h1 class="w-max bg-gray-900 border-l-4 px-2 border-primary text-lg font-bold text-primary">{project.name}</h1>
                    {#if project.url}
                        <a class="link link-primary" href={project.url}>{project.url}</a>
                    {/if}
                    <h1 class="font-light text-white">{project.description}</h1>
                    <div class="w-full h-max flex flex-wrap ">
                        {#each project.tags.split(" ") as tag}
                            <button class="bg-primary/50 m-1 px-3 py-1 rounded-full text-white font-medium">{tag}</button>
                        {/each}
                    </div>
                </div> 
                <div class="lg:col-span-2 hidden lg:block border-4 border-white rounded-xl w-full h-full">
                    <img src={project.images[0]} class="w-full rounded-xl h-max w-max max-h-[80vh] object-cover mx-auto" />
                </div>
            {/if}
            <div class="h-2 col-span-3 rounded-2xl my-4 bg-primary mx-20 "></div>
        {/each}
    </div>
</div>

<style>
  

  </style>