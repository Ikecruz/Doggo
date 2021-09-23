<template>
    <div class="container mb-3">
        <div class="row m-0">
            <div class="col-sm-6">
                <div class="p-4 d-flex justify-content-center align-items-center h-100">
                    <img src="../assets/doggo.png" alt="">
                </div>
            </div>
            <div class="col-sm-6">
                <div class="p-4 d-flex align-items-center h-100">
                    <div>
                        <h1 class="dog-title">Dog</h1>
                        <h1>/dɒɡ/ <span class="noun"> :noun</span></h1>
                        <h5>Definition:</h5>
                        <p class="definition">a domesticated carnivorous mammal that typically has a long snout, an acute sense of smell, non-retractable claws, and a barking, howling, or whining voice.</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="container mb-4">
        <div class="row m-0">
            <div class="col-12 col-sm-6 col-md-3 p-3">
                <div class="init-dog-fact">
                    <p>Scientific name</p>
                    <h4>Canis lupus familiaris</h4>
                </div>
            </div>
            <div class="col-12 col-sm-6 col-md-3 p-3">
                <div class="init-dog-fact">
                    <p>Lifespan</p>
                    <h4>10 – 13 years</h4>
                </div>
            </div>
            <div class="col-12 col-sm-6 col-md-3 p-3">
                <div class="init-dog-fact">
                    <p>Breeds</p>
                    <h4>Over 450 Dog Breeds</h4>
                </div>
            </div>
            <div class="col-12 col-sm-6 col-md-3 p-3">
                <div class="init-dog-fact">
                    <p>Eating Habits</p>
                    <h4>Omnivores</h4>
                </div>
            </div>
        </div>
    </div>

    <div class="container-fluid my-3 whitesmoke border-top border-bottom">
        <div class="d-flex justify-content-center mb-3">
            <div class="facts-header-contain">
                <h1>Dog Facts</h1>
            </div>
        </div>
        <div class="container" v-if="!facts.length">
            <div class="row m-0 p-3">
                <div class="fact-card p-3 border">
                    <div class="skeleton-loader"></div>
                    <div class="skeleton-loader"></div>
                    <div class="skeleton-loader short"></div>
                </div>
            </div>
            <div class="row m-0 p-3">
                <div class="fact-card p-3 border">
                    <div class="skeleton-loader"></div>
                    <div class="skeleton-loader"></div>
                    <div class="skeleton-loader short"></div>
                </div>
            </div>
        </div>
        <div class="container" v-else>
            <div class="row m-0 p-3" v-for="fact in facts" :key="fact.fact">
                <div class="fact-card p-3 border">
                    <p>{{fact.fact}}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {

    name: 'Homepage',
    data(){
        return{
            facts: []
        }
    },
    mounted(){
        // fetch('https://ed7c3bcd-42ef-4ca1-9b2a-b695e780eb15.mock.pstmn.io/dogfacts')
        // .then(res => res.json())
        // .then(data => this.facts = data)
        // .catch(err => console.log(err.message))
    }
}
</script>

<style>

</style>