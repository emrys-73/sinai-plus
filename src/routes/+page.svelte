<script>
    import Button from "$lib/components/ui/button/button.svelte";
    import { v4 as uuidv4 } from 'uuid';
    export function generateUUID() {
    return uuidv4();
  }


    let showAlert = false;
    let alertMessage = "";

    let next_house_number = 2;


    const houses = [
        {
            id: generateUUID(),
            name: "Biserica Elim München",
            address: "Ingolstädterstraße 43, 80807 München",
            url: "https://www.google.com/maps/place/Ingolst%C3%A4dter+Str.+43,+80807+M%C3%BCnchen/@48.1883574,11.5811965,17z/data=!3m1!4b1!4m6!3m5!1s0x479e743b45959529:0x452765343d96!8m2!3d48.1883574!4d11.5837768!16s%2Fg%2F11b8v53f9q?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false,
            time_to_next: 25,
        },
        {
            id: generateUUID(),
            name: "Kirchenstraße 15, 82194 Gröbenzell",
            address: "Kirchenstraße 15, 82194 Gröbenzell",
            url: "https://www.google.com/maps/place/Kirchenstra%C3%9Fe+15,+82194+Gr%C3%B6benzell/@48.1938593,11.370283,17z/data=!4m6!3m5!1s0x479e78d795d67319:0x3ee55bffe0d6ab3b!8m2!3d48.1938593!4d11.3728579!16s%2Fg%2F11c20y32vg?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false,
            time_to_next: 25,
        },
        {
            id: generateUUID(),
            name: "Pretzfelderstraße 47,81249 München",
            address: "Pretzfelderstraße 47,81249 München",
            url: "https://www.google.com/maps/place/Pretzfelder+Str.+47,+81249+M%C3%BCnchen/@48.1519886,11.4084161,16z/data=!3m1!4b1!4m6!3m5!1s0x479e7877ef6856c5:0xcedbd9b7cd421f20!8m2!3d48.1519886!4d11.4109964!16s%2Fg%2F11bw4326w3?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false,
            time_to_next: 25,
        },
        {
            id: generateUUID(),
            name: "Alpenstraße 12, 81541 München",
            address: "Alpenstraße 12, 81541 München",
            url: "https://www.google.com/maps/place/Alpenstra%C3%9Fe+12,+81541+M%C3%BCnchen/@48.102479,11.5484255,11.72z/data=!4m6!3m5!1s0x479ddf725107f187:0x423a4e383f639492!8m2!3d48.1168399!4d11.5824558!16s%2Fg%2F11nl59t80c?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false,
            time_to_next: 25,
        },
        {
            id: generateUUID(),
            name: "Georg-Eisenreich-Straße 6, 85540 Haar",
            address: "Georg-Eisenreich-Straße 6, 85540 Haar",
            url: "https://www.google.com/maps/place/Georg-Eisenreich-Stra%C3%9Fe+6,+85540+Haar/@48.1091485,11.7260009,17z/data=!3m1!4b1!4m6!3m5!1s0x479de1e5fecf6b91:0x382a9943d7c56156!8m2!3d48.1091485!4d11.7285812!16s%2Fg%2F11nxbn8bn1?entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false,
            time_to_next: 25,
        },

    ]

    const songs = [
        {
            id: generateUUID(),
            name: "E craciun acuma iar",
            address: "Ingolstädterstraße 43, 80807 München",
            url: "/E craciun acuma iar.pdf",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "El va domni in vesnici",
            address: "Address line 1, 567897 Munich",
            url: "/El va domni in vesnici.pdf",
            active: true,
            isStart: false,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "Engel haben Himmelslieder",
            address: "Address line 1, 567897 Munich",
            url: "/Engel haben Himmelslieder.pdf",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "Folgen wir den Hirten",
            address: "Address line 1, 567897 Munich",
            url: "/Folgen wir den Hirten.pdf",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "Freue dich Welt",
            address: "Address line 1, 567897 Munich",
            url: "/Freue dich Welt.pdf",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "Go tell it on the mountain",
            address: "Address line 1, 567897 Munich",
            url: "/Go tell it on the mountain.pdf",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "Hai deschide inima ta",
            address: "Address line 1, 567897 Munich",
            url: "/Hai deschide inima ta.pdf",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "Hört wie die Hirten singen",
            address: "Address line 1, 567897 Munich",
            url: "/Hört wie die Hirten singen.pdf",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "Immanuel Gott ist mit uns",
            address: "Address line 1, 567897 Munich",
            url: "/Immanuel Gott ist mit uns.pdf",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "Ingeri mii in ceruri canta",
            address: "Address line 1, 567897 Munich",
            url: "/Ingeri mii in ceruri canta.pdf",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "Iti cantam aleluia",
            address: "Address line 1, 567897 Munich",
            url: "/Iti cantam aleluia.pdf",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "Nun freut euch ihr Christen",
            address: "Address line 1, 567897 Munich",
            url: "/Nun freut euch ihr Christen.pdf",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "Pastorii au alergat",
            address: "Address line 1, 567897 Munich",
            url: "/Pastorii au alergat.pdf",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "S-a nascut",
            address: "Address line 1, 567897 Munich",
            url: "/S-a nascut.pdf",
            active: true,
            isStart: true,
            isEnd: false,
            visited: false,
            current: false
        },
        {
            id: generateUUID(),
            name: "Veniti sa-l cantam",
            address: "Address line 1, 567897 Munich",
            url: "/Veniti sa-l cantam.pdf",
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
    <div class="text-xl font-semibold uppercase w-full flex items-start justify-start py-0">
        Sinai
    </div>
    {#if showAlert}
        <div class="py-4 w-full px-4 bg-primary flex flex-col text-black font-black rounded-md">
            Mesaj de alertă
        </div>
    {/if}

    <div class="flex flex-col gap-0 justify-center items-center w-full py-6 bg-primary bg-opacity-100 text-black rounded-xl px-4">
        <span class="text-black font-semibold opacity-60 justify-center items-start flex flex-col w-full">
            Stația următoare
        </span>
        <span class="font-bold text-2xl flex flex-col items-start justify-center w-full text-black">
            {houses[next_house_number].name}
        </span>
    </div>

    <div class="w-full flex flex-row gap-4 justify-center items-center">
        <Button href={houses[next_house_number].url} class="w-full px-4 py-2 rounded-full text-black font-bold hover:px-16 transition-all duration-300 ease-in-out hover:font-bold">
            Afișează ruta
        </Button>

        <Button href="/muc.pdf" class="w-full px-4 py-2 bg-transparent border-[1px] border-primary font-bold hover:font-bold rounded-full hover:text-black hover:px-16 transition-all duration-300 ease-in-out">
            Descarcă harta
        </Button>
    </div>

    <div class="w-full flex flex-col justify-center items-center py-2 pt-4">
        <img src="/muc.jpeg" alt="" class="w-full h-full rounded-xl">
    </div>

    <div class="w-full flex flex-col justify-center items-center py-2">
        <div class="w-full flex flex-row justify-around items-center">
            <span class="font-bold text-lg flex flex-col items-start justify-center w-full text-white">
                Case
            </span>

            <Button href="/muc.pdf" class="w-full px-4 py-2 bg-transparent border-[1px] border-primary font-bold hover:font-bold rounded-full hover:text-black hover:px-16 transition-all duration-300 ease-in-out">
                Descarcă harta
            </Button>
        </div>

        <div class="text-white justify-center items-center flex flex-col py-6 gap-4 w-full">
            <!-- Table -->
            <table class="w-full justify-center text-white rounded-lg overflow-hidden drop-shadow-xl">
                <thead>
                  <tr class="bg-secondary text-black font-bold hidden">
                    <th class="py-1 px-4 text-start">Nume</th>
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
                Cântări
            </span>

            <Button class="w-full px-4 py-2 hidden bg-transparent border-[1px] border-primary font-bold hover:font-black rounded-full hover:text-black hover:px-16 transition-all duration-300 ease-in-out">
                Descarcă toate cântecele
            </Button>
        </div>

        <div class="text-white justify-center items-center flex flex-col py-6 gap-4 w-full">
            <!-- Table -->
            <table class="w-full justify-center text-white rounded-lg overflow-hidden drop-shadow-xl">
                <thead>
                  <tr class="bg-secondary text-black font-bold hidden">
                    <th class="py-1 px-4 text-start">Nume</th>
                  </tr>
                </thead>
                <tbody>
                  {#each songs as s, index}
                    <tr class="{index % 2 === 0 ? 'bg-[#303030]' : 'bg-[#262626]'} hover:bg-primary hover:text-black hover:font-bold">
                        <td class="py-2 px-4 border-none hover:py-4 transition-all ease-in-out duration-200">
                            <a href={s.url}>
                                {s.name}
                            </a>
                        </td>
                    </tr>
                  {/each}
                </tbody>
              </table>
        </div>
    </div>

</div>
