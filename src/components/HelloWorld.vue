<template>
    

      <div class="container-fluid">
          <div class="row justify-content-center mb-5">
              <div v-for="miembro in team" :key="miembro.codigo" class="col mt-5">
                  <div class="card text-white bg-dark">
                      <div class="d-flex justify-content-center p-2">
                          <!-- <svg width="12em" height="12em" viewBox="0 0 16 16" class="bi bi-person-bounding-box" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                          <path fill-rule="evenodd" d="M1.5 1a.5.5 0 0 0-.5.5v3a.5.5 0 0 1-1 0v-3A1.5 1.5 0 0 1 1.5 0h3a.5.5 0 0 1 0 1h-3zM11 .5a.5.5 0 0 1 .5-.5h3A1.5 1.5 0 0 1 16 1.5v3a.5.5 0 0 1-1 0v-3a.5.5 0 0 0-.5-.5h-3a.5.5 0 0 1-.5-.5zM.5 11a.5.5 0 0 1 .5.5v3a.5.5 0 0 0 .5.5h3a.5.5 0 0 1 0 1h-3A1.5 1.5 0 0 1 0 14.5v-3a.5.5 0 0 1 .5-.5zm15 0a.5.5 0 0 1 .5.5v3a1.5 1.5 0 0 1-1.5 1.5h-3a.5.5 0 0 1 0-1h3a.5.5 0 0 0 .5-.5v-3a.5.5 0 0 1 .5-.5z"
                          />
                          <path fill-rule="evenodd" d="M3 14s-1 0-1-1 1-4 6-4 6 3 6 4-1 1-1 1H3zm5-6a3 3 0 1 0 0-6 3 3 0 0 0 0 6z" />
                          </svg> -->
                      <img :src="miembro.image">
                      </div>
                      <div class="card-body">
                          <h5 class="card-title">Team member: {{miembro.codigo}} {{miembro.rol}}</h5>
                          <h5 class="card-title"> {{miembro.rombre}}</h5>
                          <p class="card-text">{{miembro.Descripcion}}
                          </p>
                      </div>
                      <div class="card-footer">
                          <small class="text-muted">Last updated 3 mins ago</small>
                      </div>
                  </div>
              </div>
          </div>
      </div>
     
</template>

<script>
import axios from 'axios';
export default {
  name: "HelloWorld",

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
    

  
};
</script>
