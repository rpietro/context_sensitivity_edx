# Can you tell me something useful?  personalized learning driven by semantic context sensitivity
<!-- Recebi o cfp do MEDINFO, vai ser em ago/2015 em SP, Deadline: dez/2014. Qualis B1 na comp. Acho que o artigo cairia bem no evento. 

legal, tem algum tempo, vamos começar e ver até onde o artigo pode chegar até a data

-->


<!--(acho que podemos trocar context sensitivity por context-awareness, termo mais difundido pela comunidade da comp) -->

## Abstract


## Introduction

While the amount and quality of research in healthcare improves every year, the usefulness of the information reaching healthcare providers lags far behind <!-- ref -->. For example <!-- add-->. This discrepancy results from a number of factors. First, most researchers do not consider healthcare providers as an information consumer, primarily focusing on their research peers. Second, the information is not provided in a way that is personalized at the individual needs of each patient. Despite these gaps,  

 * context sensitivity in education and personalization

<!-- (acho que ficou meio "solto" em relação a saúde, teria que melhorar) 

quais seriam referencias que possa ser usadas aqui?

Education is continually changing in relation to teaching processes. In recent years, technologies like mobile computing and internet have contributed to greater dissemination of information and study support materials (melhor trocar ref). Before this vast content provided by easy access to internet by students and teachers, it becomes increasingly necessary to have information filters, so it is possible to get information reliably and restricted to the domain over which the user is studying or working.
Currently, teachers assemble and distribute materials in virtual learning environments (VLE). These materials are distributed and activities are executed in these environments for all participants of the course in the same way, regardless of important context information as the student's profile, their pre-course school history (to verify the abilities of the student in course related fields), among others.
This problem is compounded in Massive Open Online Courses (MOOCs) because there is a greater variation in relation to cultural, geographical issues and variation in profiles of students. Thus, it is necessary that context information are taken into account in any way in the distribution of materials and activities for students of these courses.
-->

* use of ontologies in context sensitivity

<!--
Context awareness has been applied to various fields of application and several ways in computing. One of the most common ways of using context information in computer systems is the retrieval of information based on context. Information retrieval can be applied together with other recovery techniques and their application can be performed in the pre-filtering information recovery, post filtration in information retrieval, or the context modeling in conjunction with the modeling of information (Adomavicius et al, 2011).
Thus, context awareness has contributed in many applications to provide the retrieval of information, structured or not, to users or external systems.

Dey et al (2001) defined context as "any information que can be used to characterize the situation of an entity". Recent work have proposed some changes in how context should be treated in computer systems. In these newer definitions (Makris et al, 2013) (Perera et al, 2013), context must be inferred from a continuous flow of information of raw data which is obtained by systems. 
Context information are often represented in ontologies due to a number of factors, including level of reusability and expressivity of definitions (Strang; Popien, 2004) (Bettini et al, 2010) (Bellavista et al, 2012). 
O ambiente virtual [Open edX]() é utilizado para MOOCs em diversas universidades para diversos cursos. Na área da saúde, o [Open edX]() é utilizado pela universidade de Duke no curso de NOME_DO_CURSO para FUNCAO. PROBLEMA. 

são mais de 30 universidades - veja http://code.edx.org/
-->

In face of the previously mentioned gaps, the objective of this article is twofold. First, to enhance an existing learning management system with a semantically-driven, context sensitive framework to allow learners to have not only their courses personalized to the concepts that they individually need to learn, but to also have these concepts presented in a way that is meaningful in the context of that particular individual. Since we make use of a semantic model, a secondary objective is to create an ontology layer that provides the context sensitivity while connecting the relational and document-based databases in our learning management system.

## Methods

### Informal use case

1. instructor gathers information about concepts and situations on each of a group of learners
2. each learner receives concepts of interest to her as well as situated within her own context with the [Open edX]() system

For the purposes of this article we have used the following matrix of concepts and situations within a course to educate healthcare professionals and patients in relation to motivational interviewing. Motivational interviewing, or "a collaborative, person-centered form of guiding to elicit and strengthen motivation for change," interesting in that it is usually targetted at professionals who would like to assist others in achieving change. However, one could argue that the same methods could be used by the people themselves who want to achieve change. In other words, one could train individuals in different contexts, be it for a personal change context or in somebody else's context. In addition, motivational interviewing can also be applied to achieve change in different conceptual areas, such as health, work, among others. 



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
<!-- legal, por favor use bibtex que o pandoc integra - veja http://johnmacfarlane.net/pandoc/demos.html -->

<!--(melhor trocar ref)--> Iahnke, Silvana L.P.; Botelho, Silvia S. da Costa; Oliveira, Rodrigo R.; DOS Santos, Rafael A. Penna; Carvalho, Jônata T. “Educação Ubíqua: a tecnologia dando suporte ao processo de ensino-aprendizagem em qualquer lugar, em qualquer instante.” Rio Grande do Sul: Rio Grande: FURG. 2013
<!--(Adomavicius et al, 2011)--> Adomavicius, G., Mobasher, B., Ricci, F., & Tuzhilin, A. (2011). Context-Aware Recommender Systems, 67–80.
<!--Dey et al (2001)--> Dey A. K., Abowd G. D., Salber D., “A conceptual framework and a toolkit for supporting the rapid prototyping of context-aware applications,” Hum.-Comput. Interact., vol. 16, pp. 97–166, December 2001. http://dx.doi.org/10. 1207/S15327051HCI1623402
<!--(Makris et al, 2013)--> Makris, P., Member, S., and Skoutas, D. N., “A Survey on Context-Aware Mobile and Wireless Networking : On Networking and Computing Environments ’ Integration,” vol. 15, no. 1, pp. 362–386, 2013.
<!--(Perera et al, 2013)--> Perera, C., S. Member, A. Zaslavsky, and P. Christen, “Context Aware Computing for The Internet of Things : A Survey,” pp. 1–41, 2013.
<!--(Strang; Popien, 2004)--> Strang, Thomas, and Claudia Linnhoff-Popien. "A context modeling survey." Workshop Proceedings. 2004. 
<!--(Bettini et al, 2010)--> Bettini, C., O. Brdiczka, K. Henricksen, J. Indulska, D. Nicklas, A. Ranganathan, and D. Riboni, “A survey of context modelling and reasoning techniques,” Pervasive Mob. Comput., vol. 6, no. 2, pp. 161–180, Apr. 2010.
<!--(Bellavista et al, 2012)--> Bellavista, P., Corradi, A., Fanelli, M., & Foschini, L. (2012). A survey of context data distribution for mobile ubiquitous systems. ACM Computing Surveys, 44(4), 1–45. doi:10.1145/2333112.2333119
