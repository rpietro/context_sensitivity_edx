<!-- Recebi o cfp do MEDINFO, vai ser em ago/2015 em SP, Deadline: dez/2014. Qualis B1 na comp. Acho que o artigo cairia bem no evento. -->

# Can you tell me something useful? Personalized learning in healthcare driven by semantic context sensitivity 
<!--(acho que podemos trocar context sensitivity por context-awareness, termo mais difundido pela comunidade da comp) -->

## Abstract


## Introduction

While the amount and quality of research in healthcare improves every year, information reaching patients and the general public still lags far behind <!-- ref -->. 

<!--


-->
* context sensitivity in education and personalization

<!--
Context awareness has been applied to various fields of application and several ways in computing. One of the most common ways of using context information in computer systems is the retrieval of information based on context. Information retrieval can be applied together with other recovery techniques and their application can be performed in the pre-filtering information recovery, post filtration in information retrieval, or the context modeling in conjunction with the modeling of information (Adomavivius Survey, 2011).
Thus, context awareness has contributed in many applications to provide the retrieval of information, structured or not, to users or external systems.

Dey et al (2001) defined context as "any information que can be used to characterize the situation of an entity". Recent work have proposed some changes in how context should be treated in computer systems. In these newer definitions (Makris et al, 2013) (Perera et al, 2014), context must be inferred from a continuous flow of information of raw data which is obtained by systems. 
Context information are often represented in ontologies due to a number of factors, including level of reusability and expressivity of definitions (Strang; Popien, 2005) (Bettini et al, 2010) (Bettini et al, 2012).
-->
* use of ontologies in context sensitivity 

In face of the previously mentioned gaps, the objective of this article is twofold. First, to enhance an existing learning management system with a semantically-driven, context sensitive framework to allow learners to have not only their courses personalized to the concepts that they individually need to learn, but to also have these concepts presented in a way that is meaningful in the context of that particular individual. Since we make use of a semantic model, a secondary objective is to create an ontology layer that provides the context sensitivity while connecting the relational and document-based databases in our learning management system.

<!-- organização do artigo -->

## Methods

### Informal use case

1. instructor gathers information about concepts and situations on each of a group of learners
2. each learner receives concepts of interest to her as well as situated within her own context with the [Open edX]() system

For the purposes of this article we have used the following matrix of concepts and situations within 
<!--
situation: healthcare professionals (nurses, physicians, physical therapists) and patients

concepts: post-mastectomy treatment, post-prostatectomy treatment
 -->


### [Open edX]() description

* videos
* HTML
* exercises



### Ontology description


### Integration with existing relational and document-based databases in [Open edX]()

<!-- here to describe the layer on top of the system -->







<!-- 

"1. uma camada de ontologia que seja uma layer em cima de um banco relacional ou de documentos, com os dados sendo passados pro banco de documentos em formato de json-ld. a idéia é que daí seria possível query tudo em um único banco, eliminando a necessidade de uma triple store."

Isso, na verdade a ontologia serve como suporte (porque ela descreve os contextos e domínios), mas seria uma arquitetura que implementa o uso de ontologias (como essa camada intermediária).

"2. os dados em json-ld oferecendo sensibilidade ao contexto, ou seja, orientando como o edx modificaria a apresentação e estrutura do material educacional pra atender as necessidade individuais dos estudantes em relação aos conceitos a serem aprendidos e situações onde esses conceitos sejam aplicados"

Isso, temos que ver melhor ainda quais informações de contexto são relevantes para a adaptação. Com certeza temos o perfil de aluno e curso, mas podemos considerar outras coisas, como questões regionais e de cultura (uma aluna de doutorado do palazzo trabalhou com isso e trabalha com o Seiji (Isabela Gaparini)), mas acho que essas questões podem ser consideradas pra frente. Agora acho que a idéia é "simplificar" o contexto usado e aí depois ir aumentando a complexidade. -->


## Results


## Discussion 


## References
