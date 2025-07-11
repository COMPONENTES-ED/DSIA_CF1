<template>
  <div class="curso-main-container referencias">
    <BannerInterno
      icono="fas fa-book"
      titulo="Referencias bibliográficas"
    ></BannerInterno>
    <div class="container tarjeta tarjeta--blanca p-4 p-md-5 mb-5">
      <div v-for="ref in orderedData" :key="ref.link" class="referencias__item">
        <span v-html="ref.referencia"></span
        ><a v-if="ref.link" class="ms-1" :href="ref.link" target="_blank"
          ><span v-html="ref.link"></span
          ><i class="ms-1 fas fa-external-link-alt"></i
        ></a>
        <hr class="my-3" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Referencias',
  data: () => ({
    referencias: [
      {
        referencia:
          'Ambler, S. W. (2002). The Agile Model Driven Development (AMDD) Process.',
        link: 'https://agilemodeling.com/essays/amdd.htm',
      },
      {
        referencia:
          'Davis, A. M. (2005). Software Requirements: Objects, Functions, and States. Prentice Hall.',
        link: 'https://archive.org/details/softwarerequirem0000davi',
      },
      {
        referencia:
          'Gotel, O. C. Z., & Finkelstein, A. (1994). An analysis of the requirements traceability problem. In Proceedings of the First International Conference on Requirements Engineering (pp. 94-101). IEEE.',
        link:
          'https://www.semanticscholar.org/paper/An-analysis-of-the-requirements-traceability-Gotel-Finkelstein/ebc86c81ace4607f3f59a9053ec542cf323140a2',
      },
      {
        referencia:
          'Hoy, Z., & Xu, M. (2023, June 1). Agile Software Requirements Engineering Challenges-Solutions—A Conceptual Framework from Systematic Literature Review. Information (Switzerland). MDPI.',
        link: 'https://doi.org/10.3390/info14060322',
      },
      {
        referencia:
          'IEEE. (1998). IEEE Std 830-1998: IEEE Recommended Practice for Software Requirements Specifications.',
        link: 'https://www.math.uaa.alaska.edu/~afkjm/cs401/IEEE830.pdf',
      },
      {
        referencia:
          'Karlsson, J., & Ryan, K. (1997). A cost-value approach for prioritizing requirements. In Proceedings of the 2nd International Conference on Requirements Engineering (p. 97-104). IEEE.',
        link:
          'https://www.semanticscholar.org/paper/A-Cost-Value-Approach-for-Prioritizing-Requirements-Karlsson-Ryan/a28fdbaf1885dee544a1d4899d90994632f47564',
      },
      {
        referencia:
          'Leffingwell, D., & Widrig, D. (2003). Managing Software Requirements: A Unified Approach. Addison-Wesley.',
        link:
          'https://books.google.ca/books/about/Managing_Software_Requirements.html?id=h4pPpXp-xrEC',
      },
      {
        referencia:
          'Letaw, L. (2024, 1 enero). Requirements. Handbook Of Software Engineering Methods.',
        link:
          'https://open.oregonstate.education/setextbook/chapter/requirements/Mantilla',
      },
      {
        referencia:
          'Mantilla, G. (s. f.). Ingeniería de Requisitos acorde a K. Pohl.',
        link:
          'https://raven4j.blogspot.com/2015/08/ingenieria-de-requisitos-acorde-k-pohl.html',
      },
      {
        referencia:
          'Martin, M. (2022). What is a Functional Requirement in Software Engineering? Specification, Types, Examples. Guru99.',
        link:
          'https://www.guru99.com/functional-requirement-specification-example.html',
      },
      {
        referencia:
          'Melegati, J., Goldman, A., Kon, F., & Wang, X. (2019). A model of requirements engineering in software startups. Information and Software Technology, 109, 92–107. ',
        link: 'https://doi.org/10.1016/j.infsof.2019.02.001',
      },
      {
        referencia:
          'Serna M., E. (2021). Métodos Formales, Ingeniería de Requisitos y Pruebas del Software. Zenodo.',
        link: 'https://doi.org/10.5281/zenodo.4534359',
      },
      {
        referencia:
          'Sommerville, I. (2016). Software Engineering (10th ed.). Pearson.',
        link:
          'https://www.pearson.com/en-us/subject-catalog/p/software-engineering/P200000003258/9780137503148',
      },
    ],
  }),
  computed: {
    orderedData() {
      return [...this.referencias].sort((a, b) => {
        const afl = this.quitarAcentos(a.referencia.split(' ')[0].toLowerCase())
        const bfl = this.quitarAcentos(b.referencia.split(' ')[0].toLowerCase())
        if (afl < bfl) return -1
        if (afl > bfl) return 1
        return 0
      })
    },
  },
  methods: {
    quitarAcentos(str) {
      return str.normalize('NFD').replace(/[\u0300-\u036f]/g, '')
    },
  },
}
</script>

<style lang="sass">
.referencias
  &__item
    &:last-child
      hr
        display: none
    a
      color: $blue
      text-decoration: underline
      overflow-wrap: break-word
</style>
