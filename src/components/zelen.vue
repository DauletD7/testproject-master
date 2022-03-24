<template>
    <div>
        <div class="container mx-auto">
            <h1 class="text-center my-4 font-bold text-4xl">Zelensky Evokes U.S. History in Appeal to Congress</h1>
            <div class="sm:flex flex-wrap">
                <div class="sm:w-1/4">
                    <div class="pb-4 mb-4 border-b border-black border-solid">
                        <h5 class="text-red-600">Live</h5>
                        <h3 class="font-bold my-1">Pleads for No-Fly Zone and More Military Aid as Kyiv Is Pummeled</h3>
                        <ul class="text-gray-500 list-disc">
                            <li>
                                President Volodomyr Zelensky urged Congress to come 
                                to Ukraine’s aid, invoking the memories of Pearl Harbor 
                                and Sept. 11. “I call on you to do more,” he said.
                            </li>
                            <li>
                                After military setbacks, Russian officials said that there 
                                is “hope that a certain compromise can be reached” in talks 
                                with Ukraine. Here’s the latest.
                            </li>
                        </ul>
                    </div>
                    <h3 class="font-bold mb-1">
                        Analysis: What’s the Risk of Nuclear War? ‘It’s Not Zero.’
                    </h3>
                    <p class="text-gray-500 list-disc">A series of shifts in Russian statements has led some analysts 
                        to believe the Kremlin sees a nuclear exchange as a viable strategy.</p>
                </div>
                <div class="sm:w-1/2 px-4">      
                    <router-link to="/war">
                    <div class="relative">                        
                        <img src="https://static01.nyt.com/images/2022/03/16/multimedia/16ukraine-zelensky-flipper-02/16ukraine-zelensky-flipper-02-threeByTwoMediumAt2X-v4.jpg" 
                        alt="">
                        <p class="text-white absolute left-2 bottom-2" style="max-width: 100%;">
                            Sarahbeth Maney/The New York Times
                        </p>
                    </div>
                    </router-link>
                    <div class="p-2 border-b border-l border-r border-black border-solid">
                        <h4 class="font-bold my-1">Reporter Analysis &#187;</h4>
                        <div class="flex">
                            <div class="pr-1">
                                <img src="data:image/jpeg;base64,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" 
                                alt="">
                            </div>
                            <div>
                                <h5 class="font-bold">Valerie Hopkins</h5>
                                <p class="text-gray-500">Zelensky gave a masterclass at tailoring his messages to his audiences,
                                from of invoking the leaders and values that Americans hold so dear, 
                                to the invocations of Churchill to the British Parliament, and even his 
                                understanding of Russian pride when speaking to ordinary Russians. 
                                <span class="text-red-600">2h ago</span></p>
                                <div  class="mt-2 flex flex-wrap justify-center items-center">
                                    <div class="w-2 h-2 rounded backg bg-gray-400"></div>
                                    <div class="w-2 h-2 rounded backg bg-gray-900 mx-3"></div>
                                    <div class="w-2 h-2 rounded backg bg-gray-400"></div>
                                </div>
                            </div>
                        </div>                        
                    </div>
                </div>
                <div class="sm:w-1/4">
                    <div class="pb-4 mb-4 border-b border-black border-solid">
                        <img src="https://static01.nyt.com/images/2022/02/25/us/ukraine-maps-promo-1645801007862/ukraine-maps-promo-1645801007862-facebookJumbo-v63.png" 
                        alt="">
                        <h3 class="font-bold my-1">
                            See a map of areas of active fighting across Ukraine.
                        </h3>
                    </div>
                    <div>
                        <h3 class="font-bold">
                            Analysis: For President Vladimir
                            Putin, the war is about ethnicity and
                            empire, which have deep roots in
                            Russian history and thought.
                        </h3>
                        
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>