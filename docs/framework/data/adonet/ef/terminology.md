---
title: "Terminologie Entity Framework | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-ado"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
ms.assetid: fa2a1bd1-6118-487b-8673-eebc66b92945
caps.latest.revision: 4
author: "JennieHubbard"
ms.author: "jhubbard"
manager: "jhubbard"
caps.handback.revision: 4
---
# Terminologie Entity Framework
Cette rubrique définit des termes souvent référencés dans la documentation d'[!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].  Des liens vers des rubriques pertinentes dans lesquelles des informations supplémentaires sont disponibles sont fournis.  
  
|Terme|Définition|  
|-----------|----------------|  
|association|Définition d'une relation entre des types d'entités.<br /><br /> Pour plus d’informations, consultez [Association Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/c305169a-8af7-432f-9ba7-800a163aed41) et [type d'association](../../../../../docs/framework/data/adonet/association-type.md).|  
|jeu d'associations|Conteneur logique pour les instances d'associations du même type.<br /><br /> Pour plus d’informations, consultez [AssociationSet Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/512cbb75-cebe-4f3f-970d-3419deeff684) et [ensemble d'associations](../../../../../docs/framework/data/adonet/association-set.md).|  
|Code First|Depuis Entity Framework 4.1, vous pouvez créer un modèle par programme à l'aide du développement Code First.  Il existe deux scénarios différents pour le développement Code First.  Dans les deux cas, le développeur définit un modèle lors du codage des définitions de classe .NET Framework, puis spécifie éventuellement un mappage supplémentaire ou une configuration supplémentaire à l'aide des annotations de données ou de l'API Fluent.<br /><br /> Notez que le développement Code First fait partie d'[Entity Framework 5.0](http://go.microsoft.com/fwlink/?LinkId=234900).  Entity Framework 5.0 ne fait pas partie du .NET Framework, mais repose sur le .NET Framework 4.5.  Entity Framework 5.0 est disponible comme package [« Entity Framework »](http://go.microsoft.com/fwlink/?LinkID=215714) [NuGet](http://go.microsoft.com/fwlink/?LinkId=232488).  Pour plus d'informations, consultez [Versions et contrôle de version d'Entity Framework](http://go.microsoft.com/fwlink/?LinkID=234899).|  
|arborescence de commandes|Représentation par programme commune à toutes les requêtes [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] composées d'une de plusieurs expressions.<br /><br /> Pour plus d'informations, consultez [Vue d'ensemble d'Entity Framework](../../../../../docs/framework/data/adonet/ef/overview.md).|  
|type complexe|Classe [!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)] qui représente une propriété complexe telle que définie dans le modèle conceptuel.  Les types complexes permettent aux propriétés scalaires d'être organisées dans des entités.  Les objets complexes sont des instances de types complexes.  Pour plus d’informations, consultez [ComplexType Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/f1c2f311-9889-4b87-abd8-a94f322052e3) et [type complexe](../../../../../docs/framework/data/adonet/complex-type.md).|  
|ComplexType|Spécification d'un type de données qui représente une propriété non scalaire d'un type d'entité n'ayant pas de propriété de clé.<br /><br /> Pour plus d’informations, consultez [ComplexType Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/f1c2f311-9889-4b87-abd8-a94f322052e3) et [type complexe](../../../../../docs/framework/data/adonet/complex-type.md).|  
|modèle conceptuel|Spécification abstraite des types d'entités, types complexes, associations, conteneurs d'entités, jeux d'entités et ensembles d'associations dans le domaine d'une application générée dans le modèle EDM \([!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)]\).  Le modèle conceptuel est défini en CSDL dans le fichier .csdl.<br /><br /> Pour plus d'informations, consultez [Modélisation et mappage](../../../../../docs/framework/data/adonet/ef/modeling-and-mapping.md).|  
|fichier .csdl|Fichier XML qui contient le modèle conceptuel, exprimé en CSDL.|  
|langage CSDL \(Conceptual Schema Definition Language\)|Langage basé sur XML utilisé pour définir les types d'entité, les associations, les conteneurs d'entités, les jeux d'entités et les jeux d'associations d'un modèle conceptuel.<br /><br /> Pour plus d'informations, consultez [Spécification CSDL](../../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md).|  
|conteneur|Regroupement logique de jeux d'entités et d'ensembles d'associations.<br /><br /> Pour plus d’informations, consultez [EntityContainer Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/06d03ecb-3b7a-4e7f-95d5-b95307d47a27) et [conteneur d'entités](../../../../../docs/framework/data/adonet/entity-container.md).|  
|concurrence|Processus permettant à plusieurs utilisateurs d'accéder aux mêmes données en même temps et de les modifier.  Par défaut, [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] implémente un modèle d'accès concurrentiel optimiste.|  
|direction|Fait référence à la nature asymétrique de certaines associations.  La direction est spécifiée à l'aide des attributs `FromRole` et `ToRole` d'un élément `NavigationProperty` ou `ReferentialConstraint` dans un schéma.<br /><br /> Pour plus d’informations, consultez [NavigationProperty Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/5829a238-a50e-4c81-901d-7b54fc00f27e) et [propriété de navigation](../../../../../docs/framework/data/adonet/navigation-property.md).|  
|chargement hâtif|Processus de chargement d'un jeu spécifique d'objets connexes avec des objets explicitement demandés dans la requête.|  
|fichier .edmx|Fichier XML qui contient le modèle conceptuel \(en CSDL\), le modèle de stockage \(en SSDL\) et les mappages entre les deux \(en MSL\).  Le fichier .edmx est créé par les outils [!INCLUDE[adonet_edm](../../../../../includes/adonet-edm-md.md)]. Pour plus d'informations, consultez [.edmx File Overview](http://msdn.microsoft.com/fr-fr/f4c8e7ce-1db6-417e-9759-15f8b55155d4).|  
|end|Entité participante dans une association.<br /><br /> Pour plus d’informations, consultez [End Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/04f3c141-95bc-424b-989b-1c071b449e7c) et [terminaison d'association](../../../../../docs/framework/data/adonet/association-end.md).|  
|entité|Concept dans le domaine d'une application à partir duquel un type de données est défini.<br /><br /> Pour plus d’informations, consultez [EntityType Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/19562e9f-fd70-4b59-bc15-3e289cbb6054) et [type d'entité](../../../../../docs/framework/data/adonet/entity-type.md).|  
|EntityClient|Données [!INCLUDE[vstecado](../../../../../includes/vstecado-md.md)] indépendantes du stockage qui contiennent des classes telles que `EntityConnection`, `EntityCommand` et `EntityDataReader`.  Fonctionne avec [!INCLUDE[esql](../../../../../includes/esql-md.md)] et se connecte à des fournisseurs de données [!INCLUDE[vstecado](../../../../../includes/vstecado-md.md)] spécifiques au stockage, tels que `SqlClient`.<br /><br /> Pour plus d'informations, consultez [Fournisseur EntityClient pour Entity Framework](../../../../../docs/framework/data/adonet/ef/entityclient-provider-for-the-entity-framework.md).|  
|conteneur d'entités|Spécifie des jeux d'entités et des ensembles d'associations qui seront implémentés dans un l'espace de noms spécifié.<br /><br /> Pour plus d’informations, consultez [EntityContainer Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/06d03ecb-3b7a-4e7f-95d5-b95307d47a27) et [conteneur d'entités](../../../../../docs/framework/data/adonet/entity-container.md).|  
|EDM \(Entity Data Model\)|Ensemble de concepts qui décrivent la structure des données sous forme d'entités et de relations, indépendamment de la forme sous laquelle elles sont stockées.<br /><br /> Pour plus d'informations, consultez [Entity Data Model](../../../../../docs/framework/data/adonet/entity-data-model.md).|  
|Entity Framework|Ensemble de technologies qui prend en charge le développement d'applications logicielles orientées données en permettant aux développeurs d'utiliser des modèles conceptuels mappés à des schémas logiques dans des sources de données.<br /><br /> Pour plus d'informations, consultez [Vue d'ensemble d'Entity Framework](../../../../../docs/framework/data/adonet/ef/overview.md).|  
|jeu d'entités|Conteneur logique pour les entités d'un type donné et de ses sous\-types.  Les jeux d'entités sont mappés à des tables d'une base de données.<br /><br /> Pour plus d’informations, consultez [EntitySet Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/ec56db77-718d-4c0e-adc9-f1d33c896287) et [jeu d'entités](../../../../../docs/framework/data/adonet/entity-set.md).|  
|Entity SQL|Dialecte SQL indépendant du stockage qui fonctionne directement avec les schémas d'entité conceptuels et qui prend en charge certains concepts de modèle, tels que l'héritage et les relations.<br /><br /> Pour plus d'informations, consultez [Langage Entity SQL](../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-language.md).|  
|type d'entité|Classe [!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)] qui représente une entité telle que définie dans le modèle conceptuel.  Les types d'entités peuvent avoir des propriétés scalaires, complexes et de navigation.  Les objets sont des instances de types d'entités.  Pour plus d'informations, consultez [Utilisation d'objets](../../../../../docs/framework/data/adonet/ef/working-with-objects.md).|  
|EntityType|Spécification d'un type de données qui inclut une clé et un jeu nommé de propriétés, et qui représente un élément de niveau supérieur dans un modèle conceptuel ou un modèle de stockage.<br /><br /> Pour plus d’informations, consultez [EntityType Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/19562e9f-fd70-4b59-bc15-3e289cbb6054) et [type d'entité](../../../../../docs/framework/data/adonet/entity-type.md).|  
|chargement explicite|Lorsque des objets sont retournés par une requête, les objets connexes ne sont pas chargés en même temps.  Par défaut, ils ne sont chargés que si une requête explicite est émise à l'aide de la méthode `Load` sur une propriété de navigation.|  
|association de clé étrangère|Association entre des entités gérée via des propriétés de clé étrangère.|  
|relation d'identification|Relation où la clé primaire de l'entité principale fait également partie de la clé primaire de l'entité dépendante.  Dans ce type de relation, l'entité dépendante ne peut pas exister dans l'entité principale.|  
|association indépendante|Association entre des entités qui est représentée et suivie par un objet indépendant.|  
|clé|Attribut d'un type d'entité qui spécifie quelle propriété ou quel jeu de propriétés est utilisé pour identifier des instances uniques du type d'entité.  Représenté dans la couche objet par la classe <xref:System.Data.EntityKey>.<br /><br /> Pour plus d’informations, consultez [Key Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/0cdb1402-dbc7-4a04-a11e-5729cdf7431b) et [clé d'entité](../../../../../docs/framework/data/adonet/entity-key.md).|  
|chargement différé|Lorsque des objets sont retournés par une requête, les objets connexes ne sont pas chargés en même temps.  Ils sont en revanche chargés automatiquement lorsque la propriété de navigation est accédée.|  
|[!INCLUDE[linq_entities](../../../../../includes/linq-entities-md.md)]|Syntaxe de requête qui définit un ensemble d'opérateurs de requête qui permettent d'exprimer des opérations de parcours, de filtre et de projection d'une manière déclarative directe dans [!INCLUDE[csprcs](../../../../../includes/csprcs-md.md)] et [!INCLUDE[vbprvb](../../../../../includes/vbprvb-md.md)].<br /><br /> Pour plus d'informations, consultez [LINQ to Entities](../../../../../docs/framework/data/adonet/ef/language-reference/linq-to-entities.md).|  
|mapper|Spécification des correspondances entre des éléments d'un modèle conceptuel et des éléments d'un modèle de stockage.<br /><br /> Pour plus d'informations, consultez [Spécification MSL](../../../../../docs/framework/data/adonet/ef/language-reference/msl-specification.md).|  
|fichier .msl|Fichier XML qui contient le mappage entre le modèle conceptuel et le modèle de stockage, exprimé en MSL.|  
|langage MSL \(Mapping Specification Language\)|Langage basé sur XML utilisé pour mapper les éléments définis dans un modèle conceptuel aux éléments d'un modèle de stockage.<br /><br /> Pour plus d'informations, consultez [Spécification MSL](../../../../../docs/framework/data/adonet/ef/language-reference/msl-specification.md).|  
|fonctions de modification|Procédures stockées utilisées pour insérer, mettre à jour et supprimer des données qui se trouvent dans la source de données.  Ces fonctions sont utilisées à la place des commandes générées [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].  Les fonctions de modification sont définies par l'élément `Function` dans le modèle de stockage.  L'élément [ModificationFunctionMapping](http://msdn.microsoft.com/fr-fr/b44b5b13-9937-448b-ba36-7a0cfefea782) mappe ces fonctions de modification pour insérer, mettre à jour et supprimer des opérations sur des entités qui sont définies dans le modèle conceptuel.|  
|multiplicité|Nombre d'entités qui peuvent exister de chaque côté d'une relation, tel que défini par une association.  Également appelé cardinalité.<br /><br /> Pour plus d’informations, consultez [End Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/04f3c141-95bc-424b-989b-1c071b449e7c) et [terminaison d'association](../../../../../docs/framework/data/adonet/association-end.md).|  
|jeux d'entités multiples par type|Possibilité, pour un type d'entité, d'être défini dans plusieurs jeux d'entités.<br /><br /> Pour plus d’informations, consultez [EntitySet Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/ec56db77-718d-4c0e-adc9-f1d33c896287) et [How to: Define a Model with Multiple Entity Sets per Type](http://msdn.microsoft.com/fr-fr/61aa4fca-5ac0-4f47-9bc8-46e8c2965ef7).|  
|propriété de navigation|Propriété d'un type d'entité qui représente une relation à un autre type d'entité, tel que définie par une association.  Les propriétés de navigation sont utilisées pour retourner des objets connexes sous forme de <xref:System.Data.Objects.DataClasses.EntityCollection%601> ou de <xref:System.Data.Objects.DataClasses.EntityReference%601>, en fonction de la multiplicité à l'autre terminaison de l'association.<br /><br /> Pour plus d’informations, consultez [NavigationProperty Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/5829a238-a50e-4c81-901d-7b54fc00f27e) et [propriété de navigation](../../../../../docs/framework/data/adonet/navigation-property.md).|  
|chemin d'accès de la requête|Représentation sous forme de chaîne d'un chemin d'accès qui spécifie quels objets connexes doivent être retournés lorsqu'une requête d'objet est exécutée.  Un chemin d'accès de la requête est défini en appelant la méthode <xref:System.Data.Objects.ObjectQuery%601.Include%2A> sur un <xref:System.Data.Objects.ObjectQuery%601>.<br /><br /> Pour plus d'informations, consultez [Loading Related Objects](http://msdn.microsoft.com/fr-fr/452347d2-7b3b-44cd-9001-231299a28cb1).|  
|contexte d'objet|Représente le conteneur d'entités défini dans le modèle conceptuel.  Il contient une connexion à la source de données sous\-jacente et fournit des services tels que le suivi des modifications et la résolution d'identité.  Une extension de contexte de l'objet est représentée par une instance de la classe <xref:System.Data.Objects.ObjectContext> ou `DbContext`.<br /><br /> `DbContext` fait partie d'[Entity Framework 5.0](http://go.microsoft.com/fwlink/?LinkId=234900).  Entity Framework 5.0 ne fait pas partie du .NET Framework, mais repose sur le .NET Framework 4.5.  Entity Framework 5.0 est disponible comme package [« Entity Framework »](http://go.microsoft.com/fwlink/?LinkID=215714) [NuGet](http://go.microsoft.com/fwlink/?LinkId=232488).  Pour plus d'informations, consultez [Versions et contrôle de version d'Entity Framework](http://go.microsoft.com/fwlink/?LinkID=234899).|  
|couche objet|Types d'entité et définitions du contexte de l'objet utilisés par Entity Framework.|  
|requête d'objet|Requête exécutée dans un contexte d'objet sur un modèle conceptuel et qui retourne des données sous forme d'objets.<br /><br /> Pour plus d'informations, consultez [Object Queries](http://msdn.microsoft.com/fr-fr/0768033c-876f-471d-85d5-264884349276).|  
|mappage relationnel objet|Technique permettant de transformer des données d'une base de données relationnelle en types de données qui peuvent être utilisés dans des applications logicielles orientées objet.<br /><br /> [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] fournit des services de mappage objet\/relation en mappant des données relationnelles, telles que définies dans le modèle de stockage, aux types de données, tels que définis dans le modèle conceptuel.<br /><br /> Pour plus d'informations, consultez [Modélisation et mappage](../../../../../docs/framework/data/adonet/ef/modeling-and-mapping.md).|  
|Object Services|Services fournis par [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] qui permettent au code d'application de fonctionner sur des entités telles que des objets [!INCLUDE[dnprdnshort](../../../../../includes/dnprdnshort-md.md)].|  
|objet ignorant la persistance|Objet qui ne contient pas de logique liée au stockage des données.  Également appelé entité POCO.|  
|POCO|Objet CLR simple.  Objet qui n'hérite pas d'une autre classe ou n'implémente pas d'interface.|  
|entité POCO|Entité dans [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] qui n'hérite pas de <xref:System.Data.Objects.DataClasses.EntityObject> ou <xref:System.Data.Objects.DataClasses.ComplexObject> et n'implémente pas les interfaces [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].  Souvent, les entités POCO sont des objets domaine existants que vous utilisez dans une application [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)].  Ces entités prennent en charge l'ignorance de la persistance.  Pour plus d'informations, consultez [Working with POCO Entities](http://msdn.microsoft.com/fr-fr/5e0fb82a-b6d1-41a1-b37b-c12db61629d3).|  
|objet proxy|Objet qui dérive d'une classe POCO et est généré par [!INCLUDE[adonet_ef](../../../../../includes/adonet-ef-md.md)] pour prendre en charge le suivi des modifications et le chargement différé.  Pour plus d'informations, consultez [Requirements for Creating POCO Proxies](http://msdn.microsoft.com/fr-fr/dcdbf982-9b9d-4582-806a-64de4a1c03c8).|  
|contrainte référentielle|Contrainte définie dans un modèle conceptuel qui indique qu'une entité a une relation de dépendance à une autre entité.  Cette contrainte signifie qu'une instance d'une entité dépendante ne peut pas exister sans une instance correspondante de l'entité principale.<br /><br /> Pour plus d’informations, consultez [ReferentialConstraint Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/24f96a80-85b5-4f2e-a14c-0e3eb6796fa0) et [contrainte d'intégrité référentielle](../../../../../docs/framework/data/adonet/referential-integrity-constraint.md).|  
|relation|Connexion logique entre des entités.|  
|rôle|Nom donné à chaque `End` d'une association pour clarifier la sémantique de la relation.<br /><br /> Pour plus d’informations, consultez [End Element \(CSDL\)](http://msdn.microsoft.com/fr-fr/04f3c141-95bc-424b-989b-1c071b449e7c) et [terminaison d'association](../../../../../docs/framework/data/adonet/association-end.md).|  
|propriété scalaire|Propriété d'une entité qui mappe à un champ unique dans le modèle de stockage.|  
|entité de suivi automatique|Entité constituée à partir d'un modèle Text Template Transformation Toolkit \(T4\) qui a la capacité d'enregistrer les modifications dans les propriétés scalaires, complexes et de navigation.|  
|type simple|Type primitif utilisé pour définir des propriétés dans le modèle conceptuel.<br /><br /> Pour plus d’informations, consultez [Conceptual Model Types \(CSDL\)](http://msdn.microsoft.com/fr-fr/987b995f-e429-4569-9559-b4146744def4) et [Entity Data Model : types de données primitifs](../../../../../docs/framework/data/adonet/entity-data-model-primitive-data-types.md).|  
|entité fractionnée|Type d'entité mappé à deux types distincts dans le modèle de stockage.<br /><br /> Pour plus d'informations, consultez [How to: Define a Model with a Single Entity Mapped to Two Tables](http://msdn.microsoft.com/fr-fr/01762517-e4ab-439d-99e6-564ab7d6f3ed).|  
|modèle de stockage|Définition du modèle logique des données d'une source de données prise en charge, telle qu'une base de données relationnelle.  Le modèle de stockage est défini en SSDL dans le fichier .ssdl.<br /><br /> Pour plus d’informations, consultez [Modélisation et mappage](../../../../../docs/framework/data/adonet/ef/modeling-and-mapping.md) et [Spécification SSDL](../../../../../docs/framework/data/adonet/ef/language-reference/ssdl-specification.md).|  
|fichier .ssdl|Fichier XML qui contient le modèle de stockage, exprimé en SSDL.|  
|langage SSDL \(Store Schema Definition Language\)|Langage XML utilisé pour définir les types d'entités, associations, conteneurs d'entités, jeux d'entités et ensembles d'associations d'un modèle de stockage qui correspond le plus souvent à un schéma de la base de données.<br /><br /> Pour plus d'informations, consultez [Spécification SSDL](../../../../../docs/framework/data/adonet/ef/language-reference/ssdl-specification.md).|  
|table par hiérarchie|Méthode consistant à modéliser une hiérarchie de types dans une base de données qui inclut les attributs de tous les types de la hiérarchie d'une table.|  
|table par type|Méthode consistant à modéliser une hiérarchie de types dans une base de données qui utilise plusieurs tables avec des relations un\-à\-un pour modéliser les différents types.|  
  
## Voir aussi  
 [ADO.NET Entity Framework](../../../../../docs/framework/data/adonet/ef/index.md)   
 [Vue d'ensemble d'Entity Framework](../../../../../docs/framework/data/adonet/ef/overview.md)   
 [Mise en route](../../../../../docs/framework/data/adonet/ef/getting-started.md)   
 [Ressources Entity Framework](../../../../../docs/framework/data/adonet/ef/resources.md)