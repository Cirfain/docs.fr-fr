---
title: "&lt;MethodInstantiation&gt;, &#233;l&#233;ment (.NET Native) | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: a3355d78-2a88-4109-8521-830d7cae260a
caps.latest.revision: 17
author: "rpetrusha"
ms.author: "ronpet"
manager: "wpickett"
caps.handback.revision: 17
---
# &lt;MethodInstantiation&gt;, &#233;l&#233;ment (.NET Native)
Applique la stratégie de réflexion runtime à une méthode générique construite.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
  
<MethodInstantiation Name="method_name"  
                     Signature="method_signature"  
                     Arguments="method_arguments"  
                     Browse="policy_type"  
                     Dynamic="policy_type" />  
  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Type d'attribut|Description|  
|---------------|--------------------|-----------------|  
|`Name`|Général|Attribut requis. Spécifie le nom de la méthode.|  
|`Signature`|Général|Attribut facultatif. Spécifie les paramètres nommés de la méthode. Si plusieurs paramètres nommés sont présents, ils sont séparés par des virgules. L'attribut `Signature` est utilisé pour différencier les méthodes surchargées.|  
|`Arguments`|Général|Attribut requis. Spécifie les arguments de type générique. Si plusieurs arguments sont présents, ils sont séparés par des virgules.|  
|`Browse`|Réflexion|Attribut facultatif. Contrôle la demande d'informations sur une méthode ou l'énumération de celle-ci, mais ne permet pas d'effectuer un appel dynamique au moment de l'exécution.|  
|`Dynamic`|Réflexion|Attribut facultatif. Contrôle l'accès à un constructeur ou à une méthode au moment de l'exécution pour activer la programmation dynamique. Cette stratégie garantit que le membre peut être appelé dynamiquement au moment de l'exécution.|  
  
## <a name="name-attribute"></a>Name (attribut)  
  
|Valeur|Description|  
|-----------|-----------------|  
|*nom_méthode*|Nom de la méthode. Le type de la méthode est défini par le parent [ <> \> ](../../../docs/framework/net-native/type-element-net-native.md) ou [ <> \> ](../../../docs/framework/net-native/typeinstantiation-element-net-native.md) élément.|  
  
## <a name="signature-attribute"></a>Attribut de signature  
  
|Valeur|Description|  
|-----------|-----------------|  
|*method_signature*|Spécifie les paramètres nommés de la méthode. Si plusieurs paramètres sont présents, ils sont séparés par des virgules.|  
  
## <a name="arguments-attribute"></a>Attribut Arguments  
  
|Valeur|Description|  
|-----------|-----------------|  
|*method_arguments*|Spécifie les arguments de type générique. Si plusieurs arguments sont présents, ils sont séparés par des virgules. Chaque argument doit être composé du nom de type qualifié complet.|  
  
## <a name="all-other-attributes"></a>Tous les autres attributs  
  
|Valeur|Description|  
|-----------|-----------------|  
|*policy_setting*|Paramètre à appliquer à ce type de stratégie pour la méthode. Les valeurs possibles sont `Auto`, `Excluded`, `Included` et `Required`. Pour plus d’informations, consultez [paramètres de stratégie de Directive Runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md).|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[<>\>](../../../docs/framework/net-native/type-element-net-native.md)|Applique la stratégie de réflexion à un type et à tous ses membres.|  
|[<>\>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md)|Applique la stratégie de réflexion à un type générique construit et à tous ses membres.|  
  
## <a name="remarks"></a>Notes  
 L'élément `<MethodInstantiation>` remplace la stratégie de réflexion runtime de la méthode générique ouverte correspondante.  
  
## <a name="see-also"></a>Voir aussi  
 [Référence du fichier de Configuration (rd.xml) de Directives Runtime](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)   
 [Éléments de Directive Runtime](../../../docs/framework/net-native/runtime-directive-elements.md)   
 [Paramètres de stratégie de Directive Runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md)   
 [<>\>Élément](../../../docs/framework/net-native/method-element-net-native.md)