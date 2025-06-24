<script>
    import pentagon from "$lib/images/devcon-items/pentagon.png"

</script>
<!-- this page is super messed up, working on it (23rd june)-->

<!-- too many thing to do to figure out how to
 roll out my own tickets atm so this will redirect to eventbrite-->
<div id="welcome" class="bg-black w-screen h-214.5 relative overflow-hidden border-5 border-black">
<!-- pentagons-->
    <img class=" absolute opacity-10  top-0 left-[-350px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  top-[-330px] opacity-10 right-[210px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  bottom-[-330px] opacity-10 left-[100px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute bottom-[-300px] motion-opacity-in-0 opacity-10 left-[1550px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <div class="relative top-[100px] motion-opacity-in-0 motion-translate-y-in-100 motion-blur-in-md">
        <div class="flex flex-col lg:flex-row gap-10 justify-center">
            <a class="flex flex-col justify-start items-center gap-5 w-[95%] lg:w-[25%] bg-[#3f3301] text-slate-300 drop-shadow-2xl rounded-4xl hover:scale-105 duration-600 hover:cursor-pointer p-3" href="javascript:void(0)">
                <p class="text-center font-extrabold scale-200 text-white">Free</p>
                <button class="bg-amber-500 w-[60%] rounded-3xl text-center text-3xl font-extrabold scale-110">€ 0</button>
                <ul class="ml-2 list-disc">
                    <li>Access to all dev con talks online</li>
                    <li>Get emailed on (insert date) with link to event</li>
                </ul>
            </a>

            <a class="flex flex-col justify-start items-center gap-5 w-[95%] lg:w-[25%] bg-[#3f3301] text-slate-300 drop-shadow-2xl rounded-4xl relative top-[-1rem] scale-110 hover:scale-115 duration-600 hover:cursor-pointer p-3" href="javascript:void(0)">
                <p class="text-center font-extrabold scale-200 text-white">In-Person</p>
                <button class="bg-amber-500 w-[60%] rounded-3xl text-center text-3xl font-extrabold scale-110">€ 2</button>
                <ul class="ml-2 list-disc">
                    <li>Access to <strong>all DevCon talks in person</strong></li>
                    <li>Get emailed on <strong>October 1st</strong> with link to event</li>
                    <li><strong>Food provided</strong> at event</li>
                    <li>Access to <strong>recordings of talks</strong></li>
                    <li><strong>Goodie Bag</strong></li>
                </ul>
            </a>

            <a class="flex flex-col justify-start items-center gap-5 w-[95%] lg:w-[25%] bg-[#3f3301] text-slate-300 drop-shadow-2xl rounded-4xl hover:scale-105 duration-600 hover:cursor-pointer p-3" href="javascript:void(0)">
                <p class="text-center font-extrabold scale-200 text-white">Online</p>
                <button class="bg-amber-500 w-[60%] rounded-3xl text-center text-3xl font-extrabold scale-110">€ 2</button>
                <ul class="ml-2 list-disc">
                    <li>Access to all <strong>DevCon talks online</strong></li>
                    <li>Get emailed on <strong>(insert date)</strong> with link to event</li>
                    <li>Access to <strong>recordings of talks</strong></li>
                    <li><strong>Goodie Bag</strong></li>
                </ul>
            </a>
        </div>

        <p class="mt-4">By ordering a ticket, you agree to receive emails informing you about the event. Read the <a href="">privacy policy</a> for more information.</p>
    </div>
<!-- second div petagons-->    
</div>
