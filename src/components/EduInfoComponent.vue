<template>
    <div>
        <ul>
            <li>
                <div class="columns">
                    <div class="column">
                        <span class="colorPrimary">Mar 2023 - Ago 2023</span>
                    </div>
                    <div class="column">
                        <h4 class="has-text-left colorPrimary">Desarrollo de Aplicacion Web Front-End Trainee</h4>
                        <h6 class="has-text-left colorPrimary">Eductecno</h6>
                        <p class="has-text-justified">
                            Completé exitosamente este bootcamp de desarrollo web, adquiriendo habilidades sólidas en
                            tecnologías clave como HTML, CSS, JavaScript y frameworks modernos. Diseñé y desarrollé
                            aplicaciones web completas, demostrando mi capacidad para crear soluciones desde cero. 
                        </p>
                    </div>
                </div>
            </li>

            <li>
                <div class="columns">
                    <div class="column">
                        <span class="colorPrimary">Actualmente cursando</span>
                    </div>
                    <div class="column">
                        <h4 class="has-text-left colorPrimary">Ingenieria Electronica</h4>
                        <h6 class="has-text-left colorPrimary">Instituto Universitario Politécnico Santiago Mariño</h6>
                        <p class="has-text-justified">
                           Modalidad: A distancia.
                        </p>
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'EduInfoComponent',
    // props: {},
    data: function () {
        return {}
    },
    // computed: {},
    //methods: {},
    // watch: {},
    // components: {},
    // mixins: [],
    // filters: {},
    // -- Lifecycle Methods
    // -- End Lifecycle Methods
}
</script>

<style scoped>
ul {
    list-style: none;
}
.colorPrimary{
    color: rgb(226, 232, 240, 1)
}
</style>