# Can you tell me something useful? Personalized learning driven by semantic context awareness

<!-- Recebi o cfp do MEDINFO, vai ser em ago/2015 em SP, Deadline: dez/2014. Qualis B1 na comp. Acho que o artigo cairia bem no evento. 
legal, tem algum tempo, vamos começar e ver até onde o artigo pode chegar até a data
-->

## Abstract
Context awareness is one of the areas that are at greatest ascendancy in computing. It states that computer systems should use information from the environment to adapt their execution and content in favor of the user. In the area of ​​health education, context awareness has been used in various ways. With the adoption of Massive Open Online Courses, the use of context information can be a determining factor in the success of the courses because the contexts involved in the courses, such as the profile of students, are broader, and the adaptation based on these contexts tends to assist students and teachers. Based on a health course in the area of ​​Motivational Interviewing taught in OpenEDX platform, we modeled an ontology for the adaptation and suggestion of materials to students based on context information. Through a validation on a case study, it was possible to verify that the created ontology assisted the process of adaptation based on context.

## Introduction

Education is continually changing in relation to teaching processes. In recent years, technologies like mobile computing and internet have contributed to greater dissemination of information and study support materials <!--(Cooper; Sahami, 2013)-->. Before this vast content provided by easy access to internet by students and teachers, it becomes increasingly necessary to have information filters, so it is possible to get information reliably and restricted to the domain over which the user is studying or working <!-- (Cooper; Sahami, 2013) -->.

Currently, teachers assemble and distribute materials in virtual learning environments (VLE). These materials are distributed and activities are executed in these environments for all participants of the course in the same way, regardless of important context information as the student's profile, their pre-course school history (to verify the abilities of the student in course related fields), among others.
This problem is compounded in Massive Open Online Courses (MOOCs) because there is a greater variation in relation to cultural, geographical issues and variation in profiles of students. Thus, it is necessary that context information are taken into account in any way in the distribution of materials and activities for students of these courses <!-- (Cooper; Sahami, 2013) (Gutiírrez et al, 2014)-->.

Context awareness has been applied to various fields of application and several ways in computing. One of the most common ways of using context information in computer systems is the retrieval of information based on context. Information retrieval can be applied together with other recovery techniques and their application can be performed in the pre-filtering information recovery, post filtration in information retrieval, or the context modeling in conjunction with the modeling of information <!--(Adomavicius et al, 2011)-->.

Thus, context awareness has contributed in many applications to provide the retrieval of information, structured or not, to users or external systems.
Dey et al (2001) defined context as "any information que can be used to characterize the situation of an entity". Recent work have proposed some changes in how context should be treated in computer systems. In these newer definitions <!--(Makris et al, 2013) (Perera et al, 2013)-->, context must be inferred from a continuous flow of information of raw data which is obtained by systems. 
Context information are often represented in ontologies due to a number of factors, including level of reusability and expressivity of definitions <!--(Strang; Popien, 2004) (Bettini et al, 2010) (Bellavista et al, 2012)-->. [Open EDX]() is used in several university MOOCs, including Stanford, Harvard and MIT, and in different courses. 

<!-- trecho do texto do gustavo -->  
In healthcare domain, [Open EDX]() is used by Duke University in the Motivational Inverviewing (MI) course. MI is a patient-centered approach to behavioral changes has showed to be effective in increasing physical activity and smoking interruption. This group of techniques has been increasingly studied and it efficacy is significant in a broad range of healthy bevahiors (Cole et al, 2011).However, this group of techniques is still not popular among health practitioners and its extremely important to disseminate Motivational Interview for general health care <!--(Anstiss, 2009)-->. 
<!-- /trecho do texto do gustavo -->

While the amount and quality of research in healthcare improves every year, the usefulness of the information reaching healthcare providers lags far behind <!--Lopez-Nores et al, 2013-->. This discrepancy results from a number of factors. First, most researchers do not consider healthcare providers as an information consumer, primarily focusing on their research peers. Second, the information is not provided in a way that is personalized at the individual needs of each patient. 

In face of the previously mentioned gaps, the objective of this article is twofold. First, to enhance an existing learning management system with a semantically-driven, context sensitive framework to allow learners to have not only their courses personalized to the concepts that they individually need to learn, but to also have these concepts presented in a way that is meaningful in the context of that particular individual. Since we make use of a semantic model, a secondary objective is to create an ontology layer that provides the context sensitivity while connecting the relational and document-based databases in our learning management system.

The paper is organized as follows. Section 2 presents the main concepts related to this work as well as the description of the concepts and situations involved in the study environment. In Section 3 an ontology is presented for representing contextual information and domain related to the case study. Also in this section, the conceptual validation of the ontology and anintegration between the ontology defined in this paper and [Open EDX]() environment for information retrieval based on context are presented. Section 4 presents the main results and discussion about the contributions of this paper. Section 5 provides the concluding remarks of this work and the research agenda. 

## Methods

In the following sections we start by defining an informal use case, which is the default for the [UPON](). We then define the corresponding structure for the Open edX Platform, the ontology providing the context sensitivity, and how it is integrated into the Open edX platform, with particular detail on how the ontology serves as a layer on top of the relation and document-based databases within Open edX.

### Motivational Inverviewing

<!-- TEXTO GUSTAVO -->
Around 117 million Americans have at least one chronic health condition <!-- (Ward et al., 2012)--> and, according to the Centers for Disease Control and Prevention (CDC), 7 of the top 10 causes of death in the United States (US) are chronic diseases <!--(CDC, 2013)-->. Chronic Diseases as for example, heart disease, stroke, cancer, diabetes and obesity, have huge impact in productivity and in health costs <!--(US Department of Health and Human Services, 2014)-->. For example, the costs of just 2 conditions (heart disease and stroke) were about $315.4 billion in 2010 <!--(American Heart Association, 2014)-->.  In this context, we highlight an important particularity of chronic diseases: they are heavily dependent on bevahioral changes to be prevented or treated <!--(Rollnick et al, 2008)-->. Nonetheless, unhealthy habits are extremely common in the adult population <!--(Fryar and Chen,2012; Cogswell, 2012)--> and this contributes to the steady increase of chronic health problems. 
Two behavioral interventions, the promotion of physical activity and smoke cessation, would have a large impact on public health if properly motivated <!--(CDC, 2014)-->. Motivational interviewing (MI), a patient-centered approach to behavioral changes has showed to be effective in increasing physical activity and smoking interruption. This group of techniques has been increasingly studied and it efficacy is significant in a broad range of healthy bevahiors <!--(Cole et al, 2011)-->. However, this group of techniques is still not popular among health practitioners and its extremely important to disseminate Motivational Interview for general health care <!--(Anstiss, 2009)-->. 
MI has some guiding principles <!--(Rollnick et al., 2008)-->. Among them, we highligth the following:

#### 1) Resist the Righting Reflex

People who enter helping professions often have a powerful desire to set things right, to heal, to prevent harm and promote well-being. When seeing someone headed down the wrong path, they will usually want to get out in front of the person and say, “Stop! Turn back! There is a better way!” This is a laudable motivation; it is often what calls people into service to others. Given this motivation, the urge to correct another’s course often becomes automatic, almost reflexive.

#### 2) Understand the Patient’s Motivations

It is the patient’s own reasons for change, and not yours, that are most likely to trigger behavior change. And so a second guiding principle is to be interested in the patient’s own concerns, values, and motivations. In MI one proceeds in a way that evokes and explores patients’ perceptions about their current situations and their own motivations for change. This may sound like a prolonged process, but it need not be. It can be done within the normal length of your consultation. We believe, in fact, that if your consultation time is limited, you are better off asking patients why they would want to make a change and how they might do it rather than telling them that they should. It is the patient, rather than you, who should be voicing the arguments for behavior change. We address the practicalities, the “how to,” of this and other principles in Part II.

#### 3) Empower the Patient

It is increasingly clear that outcomes are better when patients take an active interest and role in their own health care. A fourth guiding principle in MI is empowerment—helping patients explore how they can make a difference in their own health. Again, the patient’s own ideas and resources are key here. You know that regular exercise is important, but it is your patients who know best how they could successfully build it into their daily lives. Patients in essence become your consultants on their own lives and on how best to accomplish behavior change. An important role for you in this process is to support their hope that such change is possible and can make a difference in their health. A patient who is active in the consultation, thinking aloud about the why and how of change, is more likely to do something about this afterward. You, the practitioner, are an expert in facilitating the patients’ bringing their expertise to the consultation.
<!-- /TEXTO GUSTAVO -->

<!-- ### Informal use case -->
### Motivational Scenario

Using as a basis the concepts presented earlier about the area of ​​motivational interviewing, we defined a use case based on the use of [OpenEDX]() to support a MOOC on motivational interviewing. As there are many variants in relation to the context of students and situations they may face in a motivational interviewing in everyday life. Thus, it is necessary to define contextual elements about these situations and how these elements of context can interfere on the recommendation of teaching materials in this course. The main actions to be considered in this case study are:

1. instructor gathers information about concepts and situations on each of a group of learners;
2. each learner receives concepts of interest to her as well as situated within her own context with the [Open edX]() system. 

For the purposes of this article we have used the following simplified matrix of concepts and situations within a course to educate healthcare professionals and patients in relation to motivational interviewing. Motivational interviewing, or "a collaborative, person-centered form of guiding to elicit and strengthen motivation for change" interesting in that it is usually targetted at professionals who would like to assist others in achieving change. However, one could argue that the same methods could be used by the people themselves who want to achieve change. In other words, one could train individuals in different contexts, be it for a personal change context or in somebody else's context. In addition, motivational interviewing can also be applied to achieve change in different conceptual areas, such as health, work, among others. 


|Concept to be learned |General concept learning | Learning applied to a physical exercice situation | Learning in smoking cessation situation|
|---|----|----|-----|
|Resisting the rightning reflex. |Acho que em 4-5 minutos conseguimos fazer um vídeo com as vantagens e o embasamento de resistir ao reflexo de consertar as coisas (n vai ser nada complicado). |Podemos abordar diversos exemplos, por exemplo, um paciente sedentário que fala de uma extremamente sedentária e o profissional tem q resistir. |Muitas possibilidades tb. Um paciente pode dizer q mente a quantidade q fuma ou q fuma uma quantidade absurda...|
|Listening to your patient’s motivation |Vídeo geral é tranquilo. Dizer basicamente como “ler” motivações. Tenho até vídeo pronto. |Os exemplos podem ir de fazer exercício para diminuir a ansiedade, pela saúde, p melhorar o sono, p melhorar a aparência, etc|Vários motivos podem ser abordados: motivos de saúde, preocupação com o fumo passivo do filho, questões estéticas, etc |
|Empowering your patient |Basicamente é definir estratégias juntamente com o paciente ao invés de impor soluções.| Ver qual o exercício q o paciente mais gosta, ver qual horário é melhor, ver como começar, etc. | Ver se o paciente quer medicação oral, ou selo de nicotina pela pela, em que dia parar, como diminuir a fissura.|

<!-- modifiquei um pouco -->
Based on this simplified matrix, a corresponding workflow in [Open edX]() would be roughly as follows (Figure 1):
![Figure 1](http://inf.ufrgs.br/~vmaran/img.png "Figure 1: Sequence Diagram of Learner's first interaction with the course.")
First, the learner logs into the system (1). Logged in, he recieves a survey (2) and answer it (3) choosing among the following choices:
	* which two concepts the learner would like to learn among the following choices: (a) Resisting the rightning reflex, (b) listening to your patient’s motivation, (c) empowering your patient
	* in which single situation the learner would be more likely to apply each of those concepts: (a) Physical exercise and (b) smoking cessation
Based on the responses, the system classifies the available content (4), an present the content (videos, exercises and readings) to the learner (5). For example, if the learner chooses to learn (a) the concept of resisting the rightning reflex in a situation where a patient needs to improve her physical exercise habits and (b) the concept of empowering your patient in a situation where a patient would like to stop smoking, then the ontology would determine that:
	* both general concept sections (video, exercises and readings) would be delivered to the individual courses of each learner
	* both concept sections (video, exercises and readings) in their respective situations would be delivered to the individual courses of each learner
[Open edX]() offers a tool that allows content providers to tag content <!-- Aubert et al, 2014 (precisamos confirmar esta info) -->. This way, it is possible to link the tagged context to context information and give to the learner a set of materials based on his actual context information. 

### [Open edX]() Environment
[Open edX]() é uma plataforma de ensino online utilizada por diversas universidades em diversas áreas de ensino. Sua utilização tem sido praticada principalmente na aplicação de MOOCs. A plataforma possui uma grande comunidade de desenvolvedores envolvidos, que promovem constantes soluções para integração em cursos.
OpenEDX possui uma série de recursos de apoio aos cursos definidos utilizando a plataforma como base <!-- REF -->.  

* videos
* HTML
* exercises

To extend funcionalities in [Open edX](), developers can build extensions called XBlocks. To integrate the presented ontology with [Open edX](), we propose the development of two xblocks, called Survey and Content Presentation. This extensions made communications with a web architecture, presented in Figure 2. 

![Figure 2](http://inf.ufrgs.br/~vmaran/img2.png "Figure 2: Proposed Software Architecture to Integrate Content Adaptation Based on Context in OpenEDX Environment.")

<!-- le me texto -->
Esta arquitetura utiliza dois bancos de dados para realizar o armazenamento de informações. Um deles é relacional, e armazena as informações referentes a plataforma OpenEDX, sobre cursos, alunos e ferramentas. O banco de dados com suporte a linguagem JSON por sua vez, armazena as definições de contexto utilizadas na personalização e sugestão de materiais de ensino. Desta forma, o Serviço de Gerenciamento de Bancos de Dados realiza a integração de frameworks externos como a OWL-API para o gerenciamento de ontologias e o motor de inferência Pellet. Assim, as definições utilizadas em memória por estes frameworks podem ser armazenadas e recuperadas no banco de dados.

O Engine Service realiza o controle dos serviços envolvidos na arquitetura e realiza a integração entre o Serviço de gerenciamento de bancos de dados e o processador de consultas, que por sua vez recebe requisições de consultas que envolvem informações de contexto e informações de domínio (as informações específicas do ambiente OpenEDX). Este serviço por sua vez decompõe as consultas em subconsultas, realizadas nos bancos de dados pelo serviço gerenciador de banco de dados.

O serviço de comunicação implementa interfaces de comunicação entre os Xblocks criados e integrados ao OpenEDX e a arquitetura de adaptação baseada em contexto.
Para realizar a adaptação de conteúdo baseado em contexto, e utilizar a arquitetura de forma adequada, é necessária a definição de uma ontologia que descreva:
(i) informações de contexto que podem ser levadas em consideração na adaptação e sugestão de materiais de apoio;
(ii) informações específicas do domínio de aplicação (específicas da plataforma OpenEDX). Esta modelagem é necessária para que seja possível realizar o alinhamento entre informações específicas do domínio e informações de contexto;
(iii) modelo de alinhamento entre informações de contexto e informações específicas de domínio.
Assim, a próxima seção apresenta uma modelagem baseada em ontologias para a representação de contexto e para adaptação e sugestão de materiais de apoio para a plataforma OpenEDX.
<!-- /le me texto -->

### Ontology for semantic representation of content adaptation in openEDX

<!-- Definição dos conceitos e situações na ontologia -->
The definition of the ontology was based on Methontology <!-- Fernández-López et al, 1997 -->. First of all, we made a glossary with terms and meanings of concepts, situations and contents based on the previously defined use case.
<!-- glossario de termos -->
<!-- conceitos (selecionado por item bank/lucas): reflexo endireitamento, utilizar motivação do paciente ao invés da epidemiologia/profissional, resumir o que o paciente falou; situações (selecionado por lista): adesão medicação, dieta, exercício; learning resources (videos, exercicios/itens, leituras); https://plus.google.com/hangouts/_/calendar/dmluaWNpdXNtYXJhbkBnbWFpbC5jb20.8jd70169ocma1gpkm5p5i8r32g?authuser=0 add gustavo master (A) conceitos tacitos - expressao corporal -->

### Integration with existing relational and document-based databases in [Open edX]()

<!-- here to describe the layer on top of the system -->
<!-- 
"1. uma camada de ontologia que seja uma layer em cima de um banco relacional ou de documentos, com os dados sendo passados pro banco de documentos em formato de json-ld. a idéia é que daí seria possível query tudo em um único banco, eliminando a necessidade de uma triple store."

Isso, na verdade a ontologia serve como suporte (porque ela descreve os contextos e domínios), mas seria uma arquitetura que implementa o uso de ontologias (como essa camada intermediária).

"2. os dados em json-ld oferecendo sensibilidade ao contexto, ou seja, orientando como o edx modificaria a apresentação e estrutura do material educacional pra atender as necessidade individuais dos estudantes em relação aos conceitos a serem aprendidos e situações onde esses conceitos sejam aplicados"

Isso, temos que ver melhor ainda quais informações de contexto são relevantes para a adaptação. Com certeza temos o perfil de aluno e curso, mas podemos considerar outras coisas, como questões regionais e de cultura (uma aluna de doutorado do palazzo trabalhou com isso e trabalha com o Seiji (Isabela Gaparini)), mas acho que essas questões podem ser consideradas pra frente. Agora acho que a idéia é "simplificar" o contexto usado e aí depois ir aumentando a complexidade. -->

## Results and Discussion
<!-- 
move below to Discussion:

	Although not addressed in the present article, the data provided by the same context sensitivity ontology could be applied to the following additional use cases: (1) infographics containing concepts applied to situations could be dynamically created to meet individual needs of each learner, (2) generation of automatically generated items (exercises) meeting the conceptual and situational needs for each learner, (3) guiding learning paths to feed [Learning Spaces](http://cran.r-project.org/web/packages/DAKS/index.html) -->

## Conclusions
<!-- fechamento -->

## References
<!-- legal, por favor use bibtex que o pandoc integra - veja http://johnmacfarlane.net/pandoc/demos.html -->
<!--(Adomavicius et al, 2011)--> Adomavicius, G., Mobasher, B., Ricci, F., & Tuzhilin, A. (2011). Context-Aware Recommender Systems, 67–80.
<!--Dey et al (2001)--> Dey A. K., Abowd G. D., Salber D., “A conceptual framework and a toolkit for supporting the rapid prototyping of context-aware applications,” Hum.-Comput. Interact., vol. 16, pp. 97–166, December 2001. http://dx.doi.org/10. 1207/S15327051HCI1623402
<!--(Makris et al, 2013)--> Makris, P., Member, S., and Skoutas, D. N., “A Survey on Context-Aware Mobile and Wireless Networking : On Networking and Computing Environments ’ Integration,” vol. 15, no. 1, pp. 362–386, 2013.
<!--(Perera et al, 2013)--> Perera, C., S. Member, A. Zaslavsky, and P. Christen, “Context Aware Computing for The Internet of Things : A Survey,” pp. 1–41, 2013.
<!--(Strang; Popien, 2004)--> Strang, Thomas, and Claudia Linnhoff-Popien. "A context modeling survey." Workshop Proceedings. 2004. 
<!--(Bettini et al, 2010)--> Bettini, C., O. Brdiczka, K. Henricksen, J. Indulska, D. Nicklas, A. Ranganathan, and D. Riboni, “A survey of context modelling and reasoning techniques,” Pervasive Mob. Comput., vol. 6, no. 2, pp. 161–180, Apr. 2010.
<!--(Bellavista et al, 2012)--> Bellavista, P., Corradi, A., Fanelli, M., & Foschini, L. (2012). A survey of context data distribution for mobile ubiquitous systems. ACM Computing Surveys, 44(4), 1–45. doi:10.1145/2333112.2333119
<!-- (Cooper; Sahami, 2013) --> COOPER, Steve; SAHAMI, Mehran. Reflections on stanford's moocs. Communications of the ACM, v. 56, n. 2, p. 28-30, 2013.
<!-- (Gutiírrez et al, 2014) --> Gutiírrez-Rojas, Israel, Raquel M. Crespo-García, and Carlos Delgado Kloos. "Adapting an Awareness Tool for Massive Courses: the Case of ClassON." Journal of Universal Computer Science 20.1 (2014): 24-38.
<!-- (Aubert et al, 2014) --> Aubert, Olivier, Yannick Prié, and Camila Canellas. "Leveraging video annotations in video-based e-learning." arXiv preprint arXiv:1404.4607 (2014).
<!-- Fernández-López et al, 1997 --> Fernández-López, Mariano, Asunción Gómez-Pérez, and Natalia Juristo. "Methontology: from ontological art towards ontological engineering." (1997).
<!-- Lopez-Nores et al, 2013 --> Lopez-Nores, M. (2013). Context-Aware Recommender Systems Inﬂuenced by the Users’ Health-Related Data. User Modeling and …, 153–173. doi:10.1007/978-1-4471-4778-7

<!-- Around 117 million Americans have at least one chronic health condition (Ward et al., 2012) and, according to the Centers for Disease Control and Prevention (CDC), 7 of the top 10 causes of death in the United States (US) are chronic diseases (CDC, 2013). Chronic Diseases as for example, heart disease, stroke, cancer, diabetes and obesity, have huge impact in productivity and in health costs (US Department of Health and Human Services, 2014). For example, the costs of just 2 conditions (heart disease and stroke) were about $315.4 billion in 2010 (American Heart Association, 2014)  In this context, we highlight an important particularity of chronic diseases: they are heavily dependent on bevahioral changes to be prevented or treated (Rollnick et al, 2008). Nonetheless, unhealthy habits are extremely common in the adult population (Fryar and Chen,2012; Cogswell, 2012) and this contributes to the steady increase of chronic health problems. 
Two  behavioral interventions, the promotion of physical activity and smoke cessation, would have a large impact on public health if properly motivated (CDC, 2014). For example, the majority (52%) of adults  do not practice aerobic exercise or physical activity in the recommended levels (American Heart Association, 2014) while smoking is the number one preventable cause of death in the world(REF). Motivational interviewing (MI), a patient-centered approach to behavioral changes has showed to be effective in increasing physical activity and smoking interruption. This group of techniques has been increasingly studied and it efficacy is significant in a broad range of healthy bevahiors (Cole et al, 2011).However, this group of techniques is still not popular among health practitioners and its extremely important to disseminate Motivational Interview for general health care (Anstiss, 2009). 

#Contexts (acho que os dois melhores são promoção de exercício de tabagismo, na próxima reunião posso explicar o porquê)

- Promotion of physical activity
 
Obesity is intimately associated with lack of physical activity and reduces significantly life expectancy due to increased risk to chronic illness such cardiovascular disease (Hardcastle et al, 2013). During 2009­–2010, more than one-third of adults - or about 78 million people - were obese, defined as body mass index [BMI] ≥30 kg/m2 (CDC, 2013).Promotion of physical activity correlates with weight loss and even small reductions in weight result in clinically-
-meaningful reductions in important cardiovascular risk factors (Hardcastle et al., 2013). Additionally, promotion of exercice has important consequences on mental health of the population (REF). MI showed a significant role in reducing weight and promoting physical exercice (Hardcastle et al., 2013)

 - Smoking cessation

Strong evidence shows that MI has great potential in increasing smoking cessation (Cole et al., 2012) 

# Techniques (a entrevista motivacional tem 4 princípios básicos, segundo os pesquisadores que desenvolveram essa técnica. Acredito que 3 têm um embasamento teórico substancial e poderiam ser usadas nesse momento. Aqui eu basicamente colei do livro dos inventores, falta organizar e parafrasear).

MI has some guiding principles (Rollnick et al., 2008). Among them, we highligth the following:

1) Resist the Righting Reflex

People who enter helping professions often have a powerful desire to set things right, to heal, to prevent harm and promote well-being. When seeing someone headed down the wrong path, they will usually want to get out in front of the person and say, “Stop! Turn back! There is a better way!” This is a laudable motivation; it is often what calls people into service to others. Given this motivation, the urge to correct another’s course often becomes automatic, almost reflexive.

A problem is that this first inclination can have a paradoxical effect. The reason is not that patients are flawed, recalcitrant, lazy, or in the grip of pernicious denial. Rather, it is a natural human tendency to resist persuasion. This is particularly true when one is ambivalent about something. Problem drinkers, for example, often know perfectly well that they are drinking too much and that it is having some adverse consequences. But they also enjoy drinking and don’t like to think of themselves as “having a problem,” and thus they prefer to see their drinking as reasonably normal. Virtually every problem drinker we have treated, if allowed to explore it, has felt two ways about drinking.
When a health professional takes up the “good” side of the patient’s internal argument and tries to set the patient right, what happens? If you say, “I think you are drinking too much, and should cut down or quit,” the patient’s natural response is to argue the other side of the ambivalence: “It’s not that bad, and I’m doing fine.” The temptation then is to turn up the volume, to argue all the more forcefully that the person is in trouble and needs to make a change. The patient’s response, again, is predictable.
PRACTITIONER: Well, if you did decide to exercise more, that would not only help your knee but also help you lose weight and improve your mood, you know. Exercise makes people slimmer, fitter, and feel better.

PATIENT: Yes, I know all that. But I can’t help thinking that if I exercise while my knee hurts, even with gentle things like swimming, that I am doing more damage to it, despite what you say about those studies you read….

This acting out of the patient’s internal dilemma might be therapeutic in some way were it not for another well-documented basic principle of human nature: We tend to believe what we hear ourselves say. The more patients verbalize the disadvantages of change, the more committed they become to sustaining the status quo. If you converse in a way that causes patients to defend the status quo and argue against change, you may well inadvertently decrease rather than increase the likelihood of behavior change actually happening.

We tend to believe what we hear ourselves say. The more patients verbalize the disadvantages of change, the more committed they become to sustaining the status quo.


In sum, if you are arguing for change and your patient is resisting and arguing against it, you’re in the wrong role. You are taking all the good lines. It is the patient who should be voicing the arguments for change. MI is about evoking those arguments from the patient, and that means first suppressing what may seem like the right thing to do—the righting reflex.
On many, if not most, issues of health behavior change, patients are ambivalent. They want to; they might be able to; they see good reasons to; they know they need to; and then they hit that “but.” That’s where patients’ thinking may stop unless you help them through the ambivalence. Fortunately, there is much you can do to make that happen, starting with the next guiding principle.

2)Understand Your Patient’s Motivations

It is the patient’s own reasons for change, and not yours, that are most likely to trigger behavior change. And so a second guiding principle is to be interested in the patient’s own concerns, values, and motivations. In MI one proceeds in a way that evokes and explores patients’ perceptions about their current situations and their own motivations for change. This may sound like a prolonged process, but it need not be. It can be done within the normal length of your consultation. We believe, in fact, that if your consultation time is limited, you are better off asking patients why they would want to make a change and how they might do it rather than telling them that they should. It is the patient, rather than you, who should be voicing the arguments for behavior change. We address the practicalities, the “how to,” of this and other principles in Part II.
If your consultation time is limited, you are better off asking patients why they would want to make a change and how they might do it rather than telling them that they should.

3)Empower Your Patient

It is increasingly clear that outcomes are better when patients take an active interest and role in their own health care. A fourth guiding principle in MI is empowerment—helping patients explore how they can make a difference in their own health. Again, the patient’s own ideas and resources are key here. You know that regular exercise is important, but it is your patients who know best how they could successfully build it into their daily lives. Patients in essence become your consultants on their own lives and on how best to accomplish behavior change. An important role for you in this process is to support their hope that such change is possible and can make a difference in their health. A patient who is active in the consultation, thinking aloud about the why and how of change, is more likely to do something about this afterward. You, the practitioner, are an expert in facilitating the patients’ bringing their expertise to the consultation.


A patient who is active in the consultation, thinking aloud about the why and how of change, is more likely to do something about this afterward.


Encouraging health behavior change by applying MI effectively within the space of a few minutes and in conjunction with other health care tasks is a highly skillful process. Through working in health care and listening to countless consultations over the years, we have developed deep admiration for the level of skillfulness that so many frontline clinicians already manifest in practice each and every day. Our hope in providing this book is not to displace these naturally honed skills and instincts but rather to offer what assistance we can in supporting your desire and ability to help patients change.


 #References
 1- Ward BW, Schiller JS, Goodman RA. Multiple chronic conditions among US adults: a 2012 update. Prev Chronic Dis. 2014;11:130389. DOI: http://dx.doi.org/10.5888/pcd11.130389External Web Site Icon.
 2- Centers for Disease Control and Prevention. Death and Mortality.  Avaible in: http://www.cdc.gov/nchs/fastats/deaths.htm. Accessed December, 2013.
3- Fryar CD, Chen T, Li X. Prevalence of uncontrolled risk factors for cardiovascular disease: United States, 1999–2010. NCHS Data Brief, No. 103. Hyattsville, MD: National Center for Health Statistics, Centers for Disease Control and Prevention, US Dept of Health and Human Services; 2012.
4- US Department of Health and Human Services. The Health Consequences of Smoking—50 Years of Progress: A Report of the Surgeon General. Atlanta, GA: US Dept of Health and Human Services, Centers for Disease Control and Prevention; 2014. http://www.surgeongeneral.gov/library/reports/50-years-of-progress/full-report.pdf Adobe PDF fileExternal Web Site Icon. Accessed February 7, 2014.
5- Rollnick - Motivational Interviewing
6- American Heart Association. Heart Disease and Stroke Statistics—2014 Update. AHA Statistical Update Web site. http://circ.ahajournals.org/content/early/2013/12/18/01.cir.0000441139.02102.80.full.pdf Adobe PDF fileExternal Web Site Icon. Accessed January 6, 2014.
8- Cogswell ME, Zhang Z, Carriquiry AL, et al. Sodium and potassium intakes among US adults: NHANES 2003–2008. Am J Clin Nutr. 2012;96:647-657.
CDC 2014, site.
9- Anstiss, Tim. "Motivational interviewing in primary care." Journal of Clinical Psychology in Medical Settings 16.1 (2009): 87-93.
10- Effectiveness of a motivational interviewing intervention on weight loss, physical activity and
cardiovascular disease risk factors: a randomised controlled trial with a 12-month post-intervention
follow-up. Sarah J Hardcastle1*†, Adrian H Taylor2, Martin P Bailey1, Robert A Harley1 and Martin S Hagger3†
11- Centers for Disease Control and Prevention. NCHS Data on Obesity. NCHS Fact Sheet Web site. http://www.cdc.gov/nchs/data/factsheets/factsheet_obesity.htm. Accessed December 20, 2013.
12- Steven Cole, M.D.
Michael Bogenschutz, M.D.
Dan Hungerford, Dr.P.H. Motivational
Interviewing and Psychiatry:
Use in Addiction Treatment, Risky
Drinking and Routine Practice -->
