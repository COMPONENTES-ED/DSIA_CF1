<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
  
    .titulo-principal.color-acento-contenido
      .titulo-principal__numero
        span
          i.fas.fa-info
      h1 Introducción
    
    .row.justify-content-center.mb-4
      .col-lg-3.my-lg-0.my-3.j1
        img.img-a.img-t(src='@/assets/curso/temas/4.png' alt='')    
      .col-lg-5.my-lg-0.my-3 
        .bg2.p-4.h-100.j1
          p.mb-0 La recolección y documentación de requisitos de #[i software] son fundamentales para el éxito de cualquier proyecto de desarrollo. En un entorno donde las expectativas de los clientes son cada vez más altas, es indispensable aplicar técnicas y metodologías que garanticen la precisión y claridad en la definición de necesidades. Este componente proporciona un marco estructurado para identificar, recolectar y documentar requisitos, facilitando la alineación entre los objetivos del proyecto y las expectativas del cliente.
      .col-lg-4.my-lg-0.my-3.j1
        img.img-a.img-t(src='@/assets/curso/temas/5.png' alt='')  


    .row.justify-content-center.mb-4
      .col-lg-5.my-lg-0.my-3 
        img.img-a.img-t(src='@/assets/curso/temas/6.png' alt='')  

      .col-lg-7.my-lg-0.my-3
        .bgr2.p-3.brad.j1.mb-4
          p.mb-0 El primer aspecto relevante es la recolección de datos, donde se utilizan técnicas como entrevistas, encuestas y análisis de documentos para obtener información representativa y relevante. La identificación de fuentes de información y la creación de instrumentos de recolección son pasos requeridos para asegurar que los datos capturados reflejen las necesidades reales de los usuarios y #[em stakeholders] involucrados.  
        p A continuación, se profundiza en la documentación de requisitos, destacando la importancia de especificar con claridad tanto los requisitos funcionales como los no funcionales. Se incluyen plantillas y estándares que aseguran una presentación consistente, así como técnicas de priorización y trazabilidad para gestionar el impacto de los cambios. Las herramientas de control de versiones resultan ser relevantes en el mantenimiento de la integridad de los documentos a lo largo del ciclo de vida del proyecto.

    p.mb-5 El análisis y modelado de requisitos es otra sección de este componente, donde se aplican técnicas de análisis para entender las necesidades del cliente y se desarrollan diagramas y prototipos que visualizan las soluciones propuestas. Estas representaciones permiten a los equipos validar conceptos antes de la implementación, asegurando una comprensión compartida del proyecto. 

    .row.justify-content-center.mb-5
      .col-lg-auto.j1
        img.img-a.img-t(src='@/assets/curso/temas/7.png' alt='')
      .col.pt-lg-0.pt-md-4
        .bg3.p-4.brad.h-100.j1
          p.mb-0 Finalmente, la validación de requisitos con los clientes se aborda mediante técnicas estructuradas, garantizando que las especificaciones sean correctas y completas. Este proceso incluye simulaciones y la aplicación de protocolos para hacer ajustes según sea necesario, minimizando el riesgo de errores en las etapas posteriores.    

    p.mb-5 ¡Bienvenido a este recorrido por la recolección y documentación de requisitos, donde se adentrará en las mejores prácticas para desarrollar #[em software] alineado con las expectativas del cliente!         

    .row.justify-content-center.align-items-center        
      .col-lg-12
        figure
          .video
            iframe(width="560" height="315" src="https://www.youtube.com/embed/5cqatYYb8EA?si=pCjsh2aFBb38qKXj" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen)       
</template>

<script>
export default {
  name: 'Introduccion',
  data: () => ({
    // variables de vue
  }),
}
</script>

<style lang="sass"></style>
