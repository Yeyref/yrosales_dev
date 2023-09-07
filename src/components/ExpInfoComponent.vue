<template>
    <div>
        <ul>
            <li>
                <div class="columns">
                    <div class="column colorPrimary">
                        <p>Nov 2018 - Ahora</p>
                    </div>
                    <div class="column">
                        <h4 class="has-text-left colorPrimary">Tecnico Electronico</h4>
                        <h6 class="has-text-left colorPrimary">MW Sport Welt</h6>
                        <p class="has-text-justified">
                            Planificación y desarrollo de Scoreboards para estadios profesionales,
                            municipales y gimnasios con modalidad Outdoor e Indoor, programación en C
                            de consolas electrónicas y marcadores, serigrafia de circuitos para placas de
                            control y displays.
                        </p>
                    </div>
                </div>
            </li>

            <li>
                <div class="columns">
                    <div class="column colorPrimary">
                       <p>Feb 2015 - Nov 2015</p> 
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
    name: 'ExpInfoComponent',
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