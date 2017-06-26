---
title: "Comment&#160;: configurer des informations d&#39;identification sur un service FS (Federation Service) | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "fédération"
  - "WCF, fédération"
ms.assetid: 149ab165-0ef3-490a-83a9-4322a07bd98a
caps.latest.revision: 21
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 21
---
# Comment&#160;: configurer des informations d&#39;identification sur un service FS (Federation Service)
Dans [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)], la création d'un service fédéré implique les principales procédures suivantes :  
  
1.  Configuration d'un <xref:System.ServiceModel.WSFederationHttpBinding> ou d'une liaison personnalisée similaire.[!INCLUDE[crabout](../../../../includes/crabout-md.md)] la création d'une liaison appropriée, consultez [Comment : créer une liaison WSFederationHttpBinding](../../../../docs/framework/wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md).  
  
2.  Configuration de <xref:System.ServiceModel.Security.IssuedTokenServiceCredential> qui contrôle la manière dont les jetons émis présentés au service sont authentifiés.  
  
 Cette rubrique fournit des détails sur la deuxième étape.[!INCLUDE[crabout](../../../../includes/crabout-md.md)] le fonctionnement d'un service fédéré, consultez [Fédération](../../../../docs/framework/wcf/feature-details/federation.md).  
  
### Pour définir les propriétés de IssuedTokenServiceCredential dans le code  
  
1.  Utilisez la propriété <xref:System.ServiceModel.Description.ServiceCredentials.IssuedTokenAuthentication%2A> de la classe <xref:System.ServiceModel.Description.ServiceCredentials> pour retourner une référence à une instance <xref:System.ServiceModel.Security.IssuedTokenServiceCredential>.La propriété est accessible à partir de la propriété <xref:System.ServiceModel.ServiceHostBase.Credentials%2A> de la classe <xref:System.ServiceModel.ServiceHostBase>.  
  
2.  Affectez `true` à la propriété <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.AllowUntrustedRsaIssuers%2A> si les jetons auto\-émis, tels que les cartes [!INCLUDE[infocard](../../../../includes/infocard-md.md)], doivent être authentifiés.La valeur par défaut est `false`.  
  
3.  Remplissez la collection retournée par la propriété <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.KnownCertificates%2A> avec les instances de la classe <xref:System.Security.Cryptography.X509Certificates.X509Certificate2>.Chaque instance représente un émetteur à partir duquel le service authentifiera des jetons.  
  
    > [!NOTE]
    >  Contrairement à la collection côté client retournée par la propriété <xref:System.ServiceModel.Security.X509CertificateRecipientClientCredential.ScopedCertificates%2A>, la collection des certificats connus n'est pas une collection à clé.Le service accepte les jetons que les certificats spécifiés émettent indépendamment de l'adresse du client qui a envoyé le message contenant le jeton émis \(sous réserve des contraintes supplémentaires décrites plus loin dans cette rubrique\).  
  
4.  Affectez l'une des valeurs de l'énumération <xref:System.ServiceModel.Security.X509CertificateValidationMode> à la propriété <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.CertificateValidationMode%2A>.Cette opération peut s'effectuer uniquement dans le code.La valeur par défaut est <xref:System.IdentityModel.Selectors.X509CertificateValidator.ChainTrust%2A>.  
  
5.  Si la propriété <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.CertificateValidationMode%2A> a la valeur <xref:System.ServiceModel.Security.X509CertificateValidationMode>, assignez une instance de la classe personnalisée <xref:System.IdentityModel.Selectors.X509CertificateValidator> à la propriété <xref:System.ServiceModel.Security.X509ServiceCertificateAuthentication.CustomCertificateValidator%2A>.  
  
6.  Si <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.CertificateValidationMode%2A> a la valeur `ChainTrust` ou `PeerOrChainTrust`, affectez l'une des valeurs appropriées de l'énumération <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> à la propriété <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.RevocationMode%2A>.Notez que le mode de révocation n'est pas utilisé dans les modes de validation `PeerTrust` ou `Custom`.  
  
7.  Si nécessaire, assignez une instance d'une classe personnalisée <xref:System.IdentityModel.Tokens.SamlSerializer> à la propriété <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.SamlSerializer%2A>.Un sérialiseur SAML \(Security Assertions Markup Language\) personnalisé est nécessaire, par exemple pour l'analyse des assertions SAML personnalisées.  
  
### Pour définir les propriétés de IssuedTokenServiceCredential dans la configuration  
  
1.  Créez un élément `<issuedTokenAuthentication>` en tant qu'enfant d'un élément \<`serviceCredentials`\>.  
  
2.  Affectez `true` à l'attribut `allowUntrustedRsaIssuers` de l'élément `<issuedTokenAuthentication>` en cas d'authentification d'un jeton auto\-émis, tel qu'une carte [!INCLUDE[infocard](../../../../includes/infocard-md.md)].  
  
3.  Créez un élément `<knownCertificates>` en tant qu'enfant de l'élément `<issuedTokenAuthentication>`.  
  
4.  Créez zéro ou plusieurs éléments `<add>` en tant qu'enfants de l'élément `<knownCertificates>` et spécifiez comment localiser le certificat à l'aide des attributs `storeLocation`, `storeName`, `x509FindType` et `findValue`.  
  
5.  Si nécessaire, affectez l'attribut `samlSerializer` de l'élément \<`issuedTokenAuthentication`\> au nom de type de la classe personnalisée <xref:System.IdentityModel.Tokens.SamlSerializer>.  
  
## Exemple  
 L'exemple suivant définit les propriétés de <xref:System.ServiceModel.Security.IssuedTokenServiceCredential> dans le code.  
  
 [!code-csharp[C_FederatedService#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_federatedservice/cs/source.cs#2)]
 [!code-vb[C_FederatedService#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_federatedservice/vb/source.vb#2)]  
  
 Pour qu'un service fédéré authentifie un client, les conditions suivantes doivent être vérifiées pour le jeton émis :  
  
-   Lorsque la signature numérique du jeton émis utilise un identificateur de clé de sécurité RSA, la propriété <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.AllowUntrustedRsaIssuers%2A> doit avoir la valeur `true`.  
  
-   Lorsque la signature du jeton émis utilise un numéro de série d'émetteur X.509, un identificateur de clé du sujet X.509 ou un identificateur de sécurité d'empreinte numérique X.509, le jeton émis doit être signé par un certificat de la collection retournée par la propriété <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.KnownCertificates%2A> de la classe <xref:System.ServiceModel.Security.IssuedTokenServiceCredential>.  
  
-   Lorsque le jeton émis est signé à l'aide d'un certificat X.509, le certificat doit valider suivant la sémantique spécifiée par la valeur de la propriété <xref:System.ServiceModel.Security.X509ServiceCertificateAuthentication.CertificateValidationMode%2A>, indépendamment du fait que le certificat a été envoyé à la partie de confiance en tant que <xref:System.IdentityModel.Tokens.X509RawDataKeyIdentifierClause> ou qu'il a été obtenu à partir de la propriété <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.KnownCertificates%2A>.[!INCLUDE[crabout](../../../../includes/crabout-md.md)] la validation des certificats X.509, consultez [Utilisation des certificats](../../../../docs/framework/wcf/feature-details/working-with-certificates.md).  
  
 Par exemple, si vous affectez <xref:System.ServiceModel.Security.X509CertificateValidationMode> à <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.CertificateValidationMode%2A>, les jetons émis dont le certificat de signature se trouve dans le magasin de certificats `TrustedPeople` sont authentifiés.Dans ce cas, affectez <xref:System.Security.Cryptography.X509Certificates.StoreLocation> ou <xref:System.Security.Cryptography.X509Certificates.StoreLocation> à la propriété <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.TrustedStoreLocation%2A>.Vous pouvez sélectionner d'autres modes, dont <xref:System.ServiceModel.Security.X509CertificateValidationMode>.Lorsque `Custom` est sélectionné, vous devez assigner une instance de la classe <xref:System.IdentityModel.Selectors.X509CertificateValidator> à la propriété <xref:System.ServiceModel.Security.IssuedTokenServiceCredential.CustomCertificateValidator%2A>.Le validateur personnalisé peut valider des certificats à l'aide de n'importe quel critère.[!INCLUDE[crdefault](../../../../includes/crdefault-md.md)][Comment : créer un service qui utilise un validateur de certificat personnalisé](../../../../docs/framework/wcf/extending/how-to-create-a-service-that-employs-a-custom-certificate-validator.md).  
  
## Voir aussi  
 [Fédération](../../../../docs/framework/wcf/feature-details/federation.md)   
 [Fédération et confiance](../../../../docs/framework/wcf/feature-details/federation-and-trust.md)   
 [Federation, exemple](../../../../docs/framework/wcf/samples/federation-sample.md)   
 [Comment : désactiver des sessions sécurisées sur une classe WSFederationHttpBinding](../../../../docs/framework/wcf/feature-details/how-to-disable-secure-sessions-on-a-wsfederationhttpbinding.md)   
 [Comment : créer une liaison WSFederationHttpBinding](../../../../docs/framework/wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md)   
 [Comment : créer un client fédéré](../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)   
 [Utilisation des certificats](../../../../docs/framework/wcf/feature-details/working-with-certificates.md)   
 [Modes d'authentification SecurityBindingElement](../../../../docs/framework/wcf/feature-details/securitybindingelement-authentication-modes.md)