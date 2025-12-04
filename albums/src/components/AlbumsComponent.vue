<script>
    export default{
        data(){
            return{
                albums: [
                    {
                        id: 1,
                        title: "Breezy",
                        artist: "Chris Brown",
                        release_year: 2022,
                        cover_photo: "https://upload.wikimedia.org/wikipedia/en/3/33/Chris_Brown_-_Breezy.png"
                    },
                    {
                        id: 2,
                        title: "11:11",
                        artist: "Chris Brown",
                        release_year: 2023,
                        cover_photo: "https://i.scdn.co/image/ab67616d0000b2735a4382d28ea0d58b5a422a21"
                    },
                    {
                        id: 3,
                        title: "Slime & B",
                        artist: "Chris Brown & Young Thug",
                        release_year: 2020,
                        cover_photo: "https://i.scdn.co/image/ab67616d0000b273bff2af834c576eaab5bc4d0f"
                    },
                    {
                        id: 4,
                        title: "Indigo",
                        artist: "Chris Brown",
                        release_year: 2019,
                        cover_photo: "https://upload.wikimedia.org/wikipedia/en/1/1f/Chris_Brown_-_Indigo.png"
                    },
                    {
                        id: 5,
                        title: "Heartbreak on a Full Moon",
                        artist: "Chris Brown",
                        release_year: 2017,
                        cover_photo: "https://i.scdn.co/image/ab67616d0000b27368c24e946ccd186517b43067"
                    },
                    {
                        id: 6,
                        title: "Sethifayd Khetshist",
                        artist: "SIZA M",
                        release_year: 2023,
                        cover_photo: "https://i.scdn.co/image/ab67616d0000b27356898d84ffb500b017e8bee3"
                    },
                    {
                        id: 7,
                        title: "X",
                        artist: "Chris Brown",
                        release_year: 2014,
                        cover_photo: "https://i.scdn.co/image/ab67616d00001e02b37e6176a034d4470304d706"
                    },
                    {
                        id: 8,
                        title: "F.A.M.E.",
                        artist: "Chris Brown",
                        release_year: 2011,
                        cover_photo: "https://i.scdn.co/image/ab67616d0000b2730a1d20ec09cab4bb17a36aab"
                    }
                ]
            }
        }
    }
</script>
<template>
    <div class="cards">
        <div class="card" v-for="album in albums" :key="album.id" style="width: 18rem;">
            <img :src="album.cover_photo" class="card-img-top" :alt="album.title">
            <div class="card-body">
                <h5 class="card-title">{{album.title}}</h5>
                <p class="card-text">Released in {{album.release_year}}</p>
                <a href="#" class="btn btn-primary">{{album.artist}}</a>
            </div>
        </div>
    </div>
</template>
<style>
.cards{
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
}
</style>