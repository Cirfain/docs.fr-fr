---
title: "Comment : appeler le compilateur de ligne de commande (Visual Basic)"
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- command-line arguments
- vbc.exe
- Visual Basic compiler, starting
- command line [Visual Basic], arguments
ms.assetid: 0fd9a8f6-f34e-4c35-a49d-9b9bbd8da4a9
caps.latest.revision: "28"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 5c69860ede5620272e67bde435e6e6fa08cc81bc
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-invoke-the-command-line-compiler-visual-basic"></a>Comment : appeler le compilateur de ligne de commande (Visual Basic)
Vous pouvez appeler le compilateur de ligne de commande en tapant le nom de son fichier exécutable dans la ligne de commande, également appelée invite de commande MS-DOS. Si vous compilez à partir de l’invite de commandes Windows par défaut, vous devez taper le chemin d’accès complet au fichier exécutable. Pour remplacer ce comportement par défaut, vous pouvez utiliser la [!INCLUDE[vsprvs](~/includes/vsprvs-md.md)] invite de commandes, ou modifier la variable d’environnement PATH. Deux vous permettent de compiler à partir de n’importe quel répertoire en tapant simplement le nom du compilateur.  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-invoke-the-compiler-using-the-visual-studio-command-prompt"></a>Pour appeler le compilateur à l’aide de l’invite de commandes Visual Studio  
  
1.  Ouvrez le dossier de programme Visual Studio Tools dans le groupe de programmes Microsoft Visual Studio.  
  
2.  Vous pouvez utiliser la [!INCLUDE[vsprvs](~/includes/vsprvs-md.md)] invite de commandes pour accéder au compilateur à partir de n’importe quel répertoire sur votre ordinateur, si Visual Studio est installé.  
  
3.  Appeler le [!INCLUDE[vsprvs](~/includes/vsprvs-md.md)] invite de commandes.  
  
4.  À la ligne de commande, tapez `vbc.exe` *sourceFileName* puis appuyez sur ENTRÉE.  
  
     Par exemple, si vous avez stocké votre code source dans un répertoire appelé `SourceFiles`, vous exécuteriez l’invite de commandes et le type `cd SourceFiles` pour accéder à ce répertoire. Si le répertoire contenait un fichier source nommé `Source.vb`, vous pouvez le compiler en tapant `vbc.exe Source.vb`.  
  
### <a name="to-set-the-path-environment-variable-to-the-compiler-for-the-windows-command-prompt"></a>Pour définir la variable d’environnement PATH pour le compilateur de l’invite de commandes Windows.  
  
1.  Utilisez la fonctionnalité de recherche de Windows pour rechercher Vbc.exe sur votre disque local.  
  
     Le nom exact du répertoire où se trouve le compilateur dépend de l’emplacement du répertoire Windows et de la version de « Installé le .NET Framework ». Si vous avez plusieurs versions de « Installé le .NET Framework », vous devez déterminer la version à utiliser (en général, la version la plus récente).  
  
2.  À partir de votre **Démarrer** Menu, avec le bouton droit **poste**, puis cliquez sur **propriétés** dans le menu contextuel.  
  
3.  Cliquez sur le **avancé** onglet, puis cliquez sur **Variables d’environnement**.  
  
4.  Dans le **système** volet variables, sélectionnez **chemin d’accès** à partir de la liste et cliquez sur **modifier**.  
  
5.  Dans le **modifier le système** boîte de dialogue Variable déplacer le point d’insertion à la fin de la chaîne dans le **valeur de la Variable** champ et tapez un point-virgule ( ;) suivi du nom complet du répertoire trouvé à l’étape 1.  
  
6.  Cliquez sur **OK** pour confirmer vos modifications et fermer les boîtes de dialogue.  
  
     Après avoir modifié la variable d’environnement PATH, vous pouvez exécuter la [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] compilateur à l’invite de commandes Windows à partir de n’importe quel répertoire sur l’ordinateur.  
  
### <a name="to-invoke-the-compiler-using-the-windows-command-prompt"></a>Pour appeler le compilateur à l’aide de l’invite de commandes Windows  
  
1.  À partir de la **Démarrer** menu, cliquez sur le **Accessoires** , puis ouvrez le **invite de commandes Windows**.  
  
2.  À la ligne de commande, tapez `vbc.exe` *sourceFileName* puis appuyez sur ENTRÉE.  
  
     Par exemple, si vous avez stocké votre code source dans un répertoire appelé `SourceFiles`, vous exécuteriez l’invite de commandes et le type `cd SourceFiles` pour accéder à ce répertoire. Si le répertoire contenait un fichier source nommé `Source.vb`, vous pouvez le compiler en tapant `vbc.exe Source.vb`.  
  
## <a name="see-also"></a>Voir aussi  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [Compilation conditionnelle](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
