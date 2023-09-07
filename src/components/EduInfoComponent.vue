<template>
    <div>
        <ul>
            <li>
                <div class="columns">
                    <div class="column colorPrimary">
                        <p>Mar 2023 - Ago 2023</p>
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
                    <div class="column colorPrimary">
                        <p>Actualmente cursando</p>
                    </div>
                    <div class="column">
                        <h4 class="has-text-left colorPrimary">Tecnico Instalador Junior</h4>
                        <h6 class="has-text-left colorPrimary">Vehicule Security Resources de Venezuela</h6>
                        <p class="has-text-justified">
                            Técnico Instalador Junior de dispositivos gps y radiofrecuencia de rastreo y monitoreo.
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
}
</script>

<style scoped>
ul {
    list-style: none;
    margin: 0;
}
.colorPrimary{
    color: rgb(226, 232, 240, 1)
}
</style>
