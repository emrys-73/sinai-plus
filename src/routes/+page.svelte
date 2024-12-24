<script>
    import Button from "$lib/components/ui/button/button.svelte";
    import { v4 as uuidv4 } from 'uuid';
    export function generateUUID() {
    return uuidv4();
  }


    let showAlert = false;


    const houses = [
        {
            id: generateUUID(),
            name: "House 1",
            address: "Address line 1, 567897 Munich",
            url: "https://www.google.com/maps/place/Biserica+Lui+Dumnezeu+Elim+M%C3%BCnchen/@48.187656,11.5841412,16z/data=!3m1!5s0x479e743b45b8b5a3:0x99d400c2da8f424c!4m6!3m5!1s0x479e743b45bfffff:0xd137c2e364737a7f!8m2!3d48.1883574!4d11.5837768!16s%2Fg%2F11fp1t5bn0?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "House 2",
            address: "Address line 1, 567897 Munich",
            url: "https://www.google.com/maps/place/Biserica+Lui+Dumnezeu+Elim+M%C3%BCnchen/@48.187656,11.5841412,16z/data=!3m1!5s0x479e743b45b8b5a3:0x99d400c2da8f424c!4m6!3m5!1s0x479e743b45bfffff:0xd137c2e364737a7f!8m2!3d48.1883574!4d11.5837768!16s%2Fg%2F11fp1t5bn0?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "House 1",
            address: "Address line 1, 567897 Munich",
            url: "https://www.google.com/maps/place/Biserica+Lui+Dumnezeu+Elim+M%C3%BCnchen/@48.187656,11.5841412,16z/data=!3m1!5s0x479e743b45b8b5a3:0x99d400c2da8f424c!4m6!3m5!1s0x479e743b45bfffff:0xd137c2e364737a7f!8m2!3d48.1883574!4d11.5837768!16s%2Fg%2F11fp1t5bn0?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "House 1",
            address: "Address line 1, 567897 Munich",
            url: "https://www.google.com/maps/place/Biserica+Lui+Dumnezeu+Elim+M%C3%BCnchen/@48.187656,11.5841412,16z/data=!3m1!5s0x479e743b45b8b5a3:0x99d400c2da8f424c!4m6!3m5!1s0x479e743b45bfffff:0xd137c2e364737a7f!8m2!3d48.1883574!4d11.5837768!16s%2Fg%2F11fp1t5bn0?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "House 1",
            address: "Address line 1, 567897 Munich",
            url: "https://www.google.com/maps/place/Biserica+Lui+Dumnezeu+Elim+M%C3%BCnchen/@48.187656,11.5841412,16z/data=!3m1!5s0x479e743b45b8b5a3:0x99d400c2da8f424c!4m6!3m5!1s0x479e743b45bfffff:0xd137c2e364737a7f!8m2!3d48.1883574!4d11.5837768!16s%2Fg%2F11fp1t5bn0?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "House 1",
            address: "Address line 1, 567897 Munich",
            url: "https://www.google.com/maps/place/Biserica+Lui+Dumnezeu+Elim+M%C3%BCnchen/@48.187656,11.5841412,16z/data=!3m1!5s0x479e743b45b8b5a3:0x99d400c2da8f424c!4m6!3m5!1s0x479e743b45bfffff:0xd137c2e364737a7f!8m2!3d48.1883574!4d11.5837768!16s%2Fg%2F11fp1t5bn0?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },

    ]

    const songs = [
        {
            id: generateUUID(),
            name: "House 1 - Biserica Elim München",
            address: "Ingolstädterstraße 43, 80807 München",
            url: "https://www.google.com/maps/place/Biserica+Lui+Dumnezeu+Elim+M%C3%BCnchen/@48.187656,11.5841412,16z/data=!3m1!5s0x479e743b45b8b5a3:0x99d400c2da8f424c!4m6!3m5!1s0x479e743b45bfffff:0xd137c2e364737a7f!8m2!3d48.1883574!4d11.5837768!16s%2Fg%2F11fp1t5bn0?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "House 2",
            address: "Address line 1, 567897 Munich",
            url: "https://www.google.com/maps/place/Biserica+Lui+Dumnezeu+Elim+M%C3%BCnchen/@48.187656,11.5841412,16z/data=!3m1!5s0x479e743b45b8b5a3:0x99d400c2da8f424c!4m6!3m5!1s0x479e743b45bfffff:0xd137c2e364737a7f!8m2!3d48.1883574!4d11.5837768!16s%2Fg%2F11fp1t5bn0?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: false,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "House 1",
            address: "Address line 1, 567897 Munich",
            url: "https://www.google.com/maps/place/Biserica+Lui+Dumnezeu+Elim+M%C3%BCnchen/@48.187656,11.5841412,16z/data=!3m1!5s0x479e743b45b8b5a3:0x99d400c2da8f424c!4m6!3m5!1s0x479e743b45bfffff:0xd137c2e364737a7f!8m2!3d48.1883574!4d11.5837768!16s%2Fg%2F11fp1t5bn0?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "House 1",
            address: "Address line 1, 567897 Munich",
            url: "https://www.google.com/maps/place/Biserica+Lui+Dumnezeu+Elim+M%C3%BCnchen/@48.187656,11.5841412,16z/data=!3m1!5s0x479e743b45b8b5a3:0x99d400c2da8f424c!4m6!3m5!1s0x479e743b45bfffff:0xd137c2e364737a7f!8m2!3d48.1883574!4d11.5837768!16s%2Fg%2F11fp1t5bn0?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "House 1",
            address: "Address line 1, 567897 Munich",
            url: "https://www.google.com/maps/place/Biserica+Lui+Dumnezeu+Elim+M%C3%BCnchen/@48.187656,11.5841412,16z/data=!3m1!5s0x479e743b45b8b5a3:0x99d400c2da8f424c!4m6!3m5!1s0x479e743b45bfffff:0xd137c2e364737a7f!8m2!3d48.1883574!4d11.5837768!16s%2Fg%2F11fp1t5bn0?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "House 1",
            address: "Address line 1, 567897 Munich",
            url: "https://www.google.com/maps/place/Biserica+Lui+Dumnezeu+Elim+M%C3%BCnchen/@48.187656,11.5841412,16z/data=!3m1!5s0x479e743b45b8b5a3:0x99d400c2da8f424c!4m6!3m5!1s0x479e743b45bfffff:0xd137c2e364737a7f!8m2!3d48.1883574!4d11.5837768!16s%2Fg%2F11fp1t5bn0?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },

    ]


//     Start 19:20 Ingolstädterstraße 43, 80807 München
// 20:00 - 20:20 Birkenstraß 22, 85419 Mauern 
// 20:45 - 21:15 Waldkirchener Straße 9, 84030 Landshut 
// 21:30 - 21:50 Schleienweg 5, 84174 Eching 
// 22:00 - 22:20 Hauptstraße 21, 84172 Buch am Erlbach
// 22:30 - 22:50 Lilienweg 3, 84174 Eching
// 23:00 - 23:30 Schmiedleiten 84174 Haunwang
// 23:40 - 24:00 Hauptstraße 10, 84174 Eching Viecht
// 24:00 - Open End Eichenstraße 8, 84174 Eching

// Start 19:15 Ingolstädterstraße 43, 80807 München
// 19:40 - 20:00 Kirchenstraße 15, 82194 Gröbenzell (25min)
// 20:15 - 20:35 Pretzfelderstraße 47,81249 München (15 min)
// 21:00 - 21:20 Alpenstraße 12, 81541 München (25 min)
// 21:40 - 22:00 Georg-Eisenreich-Straße 6, 85540 Haar (20 min)

</script>


<div class="bg-[#1C1C1C] w-full min-h-screen flex flex-col justify-start items-center text-white px-4 py-6 gap-6">
    <div class=" text-xl font-semibold uppercase w-full flex items-start justify-start py-0">
        Sinai
    </div>
    {#if showAlert}
        <div class="py-4 w-full px-4 bg-primary flex flex-col text-black font-black rounded-md">
            Alert message
        </div>
    {/if}

    <div class="flex flex-col gap-0 justify-center items-center w-full">
        <span class="text-[#959595] font-bold justify-center items-start flex flex-col w-full">
            Nächster Halt
        </span>
        <span class="font-bold text-lg flex flex-col items-start justify-center w-full text-white">
            Haus 4
        </span>
    </div>

    <div class="w-full flex flex-row gap-4 justify-center items-center">
        <Button class="w-full px-4 py-2 rounded-full text-black font-bold hover:px-16 transition-all duration-300 ease-in-out hover:font-bold">
            Get Directions
        </Button>

        <Button class="w-full px-4 py-2 bg-transparent border-[1px] border-primary font-bold hover:font-bold rounded-full hover:text-black hover:px-16 transition-all duration-300 ease-in-out">
            Download map
        </Button>
    </div>

    <div class="w-full flex flex-col justify-center items-center py-2 pt-4">
        <img src="/muc.jpeg" alt="" class="w-full h-full rounded-xl">
    </div>

    <div class="w-full flex flex-col justify-center items-center py-2">
        <div class="w-full flex flex-row justify-around items-center">
            <span class="font-bold text-lg flex flex-col items-start justify-center w-full text-white">
                Houses
            </span>

            <Button class="w-full px-4 py-2 bg-transparent border-[1px] border-primary font-bold hover:font-black rounded-full hover:text-black hover:px-16 transition-all duration-300 ease-in-out">
                Karte runterladen
            </Button>
        </div>

        <div class="text-white justify-center items-center flex flex-col py-6 gap-4 w-full">
            <!-- Table -->
            <table class="w-full justify-center text-white rounded-lg overflow-hidden drop-shadow-xl">
                <thead>
                  <tr class="bg-secondary text-black font-bold hidden">
                    <th class="py-1 px-4 text-start">Name</th>
                  </tr>
                </thead>
                <tbody>
                  {#each houses as h, index}
                    <tr class="{index % 2 === 0 ? 'bg-[#303030]' : 'bg-[#262626]'} hover:bg-primary hover:text-black hover:font-bold">
                        <td class="py-2 px-4 border-none hover:py-4 transition-all ease-in-out duration-200">
                            <a href={h.url}>
                                {h.name}
                            </a>
                        </td>
                    </tr>
                  {/each}
                </tbody>
              </table>
        </div>
    </div>

    <div class="w-full flex flex-col justify-center items-center py-2">
        <div class="w-full flex flex-row justify-around items-center">
            <span class="font-bold text-lg flex flex-col items-start justify-center w-full text-white">
                Lieder
            </span>

            <Button class="w-full px-4 py-2 bg-transparent border-[1px] border-primary font-bold hover:font-black rounded-full hover:text-black hover:px-16 transition-all duration-300 ease-in-out">
                Alle Lieder runterladen
            </Button>
        </div>

        <div class="text-white justify-center items-center flex flex-col py-6 gap-4 w-full">
            <!-- Table -->
            <table class="w-full justify-center text-white rounded-lg overflow-hidden drop-shadow-xl">
                <thead>
                  <tr class="bg-secondary text-black font-bold hidden">
                    <th class="py-1 px-4 text-start">Name</th>
                  </tr>
                </thead>
                <tbody>
                  {#each houses as h, index}
                    <tr class="{index % 2 === 0 ? 'bg-[#303030]' : 'bg-[#262626]'} hover:bg-primary hover:text-black hover:font-bold">
                        <td class="py-2 px-4 border-none hover:py-4 transition-all ease-in-out duration-200">
                            <a href={h.url}>
                                {h.name}
                            </a>
                        </td>
                    </tr>
                  {/each}
                </tbody>
              </table>
        </div>
    </div>

</div>