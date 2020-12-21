<template>
<div>
    <div class="container-fluid">
        <div class="row mt-md-5 mt-sm-5 mt-xs-5">
            <div v-for="(art,indice) of datos" :key="art.id" class="col-lg-6 col-xs-12 border">
                <div v-if="indice<=3">
                <div  class="d-flex justify-content-center align-items-center">

                    <div class="p-3">
                        <svg width="12em" height="12em" viewBox="0 0 16 16" class="bi bi-alarm-fill" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                            <path fill-rule="evenodd" d="M6 .5a.5.5 0 0 1 .5-.5h3a.5.5 0 0 1 0 1H9v1.07a7.001 7.001 0 0 1 3.274 12.474l.601.602a.5.5 0 0 1-.707.708l-.746-.746A6.97 6.97 0 0 1 8 16a6.97 6.97 0 0 1-3.422-.892l-.746.746a.5.5 0 0 1-.707-.708l.602-.602A7.001 7.001 0 0 1 7 2.07V1h-.5A.5.5 0 0 1 6 .5zM.86 5.387A2.5 2.5 0 1 1 4.387 1.86 8.035 8.035 0 0 0 .86 5.387zM11.613 1.86a2.5 2.5 0 1 1 3.527 3.527 8.035 8.035 0 0 0-3.527-3.527zM8.5 5.5a.5.5 0 0 0-1 0v3.362l-1.429 2.38a.5.5 0 1 0 .858.515l1.5-2.5A.5.5 0 0 0 8.5 9V5.5z"
                            />
                        </svg>
                    </div>

                    <div class="p-2">
                        <p>
                            {{art.nombre}}
                        </p>
                    </div>

                </div>
                <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
                    <button type="button" class="btn btn-outline-info">Info</button>
                </div>
                </div>
            </div>
        </div>
    </div>
    <div class="container-fluid">
        <div class="row justify-content-center mb-5">
            <div v-for="miembro in team" :key="miembro.codigo" class="col mt-5">
                     <div class="card text-white bg-dark">
                        <div class="d-flex justify-content-center p-2">
                            <img :src="miembro.image">
                        </div>
                        <div class="card-body">
                            <h5 class="card-title">Team member: {{miembro.codigo}} {{miembro.rol}}</h5>
                            <h5 class="card-title"> {{miembro.nombre}}</h5>
                            <p class="card-text">{{miembro.descripcion}}
                            </p>
                    </div>
                </div>
            </div>
        </div>
    </div>
    </div>
</template>


<script>
import axios from 'axios';
export default {
     data() {
        return {
            datos: null,
            team: [{
          codigo: 1,
          nombre: "Santiago Andrés Millan Pardo",
          descripcion: "Estudiante de Ingenieria de Telecomunicaciones en la Universidad Santo Tomas. Apacionado por el deporte,desarrollo de herramientas tecnologias y la gestion de procesos. Amor por las dos ruedas.",
          rol: "Desarrollador Backend",
          image: "https://i.imgur.com/z4eUwdT.jpg",
        },
        {
          codigo: 2,
          nombre: "Cristhian Daniel Diaz Salazar",
          descripcion: "Ingeniero Industrial de la Universidad Tecnológica de Pereira. Me dedico a administrar hoteles en Pereira. Apasionado por la ciencia, la tecnología y los sistemas de información. Mi pasatiempo favorito es jugar videojuegos.",
          rol: "Scrum Master",
          image: "https://i.imgur.com/0ULDIO2.jpg",
        },
        {
          codigo: 3,
          nombre: "Miguel Enrique Marquez Aldana",
          descripcion: "Supervisor de prospección geofísica con más de 16 años de experiencia en la planeación, supervisión y ejecución de registro de ondas sísmicas, con habilidad para el trabajo en diferentes tipos de terreno y en un ambiente multicultural.",
          rol: "Tester",
          image: "https://i.imgur.com/CPnYLi6.jpg?1",
        },
        {
          codigo: 4,
          nombre: "Diego Luis Soto Mendoza",
          descripcion: "Ingeniero electrónico de la Universidad de los Llanos, estudiante de especialización en instrumentación y control industrial. Apasionado por la tecnología, la música y los videojuegos.",
          rol: "FrontEnd",
          image: "https://media-exp1.licdn.com/dms/image/C4E03AQHZMtBSKiBNYA/profile-displayphoto-shrink_200_200/0?e=1613001600&v=beta&t=jfWKoWUKkuFsNUV5AZGwCvOR4DZERUBJQ8AnEKzb3yw",
        },
        {
          codigo: 5,
          nombre: "Alejandro Rendón Blandón",
          descripcion: "Ingeniero electrónico, especialista en Telecomunicaciones, especialista en Gerencia de Proyectos de la Universidad Pontificia Bolivariana en Medellín. Mi pasatiempo favorito es viajar en moto por todo el mundo, compartiendo con mis amigos.",
          rol: "Product Owner",
          image: "https://media-exp1.licdn.com/dms/image/C4D03AQFdkfPuDWfTbA/profile-displayphoto-shrink_200_200/0/1542999635999?e=1613001600&v=beta&t=ae7jEsQ4hQlv0B3Ql7_8OJxGBQjdzaIjvUxozVG5hFk",
        }]
        };
    },
    mounted() {
     axios.get('articulo/list')
    .then(response => (this.datos = response.data));

    },
    
}
</script>