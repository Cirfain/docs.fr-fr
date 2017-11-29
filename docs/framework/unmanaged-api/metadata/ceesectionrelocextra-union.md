---
title: CeeSectionRelocExtra, union
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CeeSectionRelocExtra Union
api_location: mscoree.dll
api_type: COM
f1_keywords: CeeSectionRelocExtra
helpviewer_keywords: CeeSectionRelocExtra union [.NET Framework metadata]
ms.assetid: d9568cf6-7f98-4cd6-ab36-0a2bd509afcc
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: c5b584ced996b31be6656082af3f64a19b1f223c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/18/2017
---
# <a name="ceesectionrelocextra-union"></a><span data-ttu-id="e61b6-102">CeeSectionRelocExtra, union</span><span class="sxs-lookup"><span data-stu-id="e61b6-102">CeeSectionRelocExtra Union</span></span>
<span data-ttu-id="e61b6-103">Représente un offset d’adresse qui est utilisé par le [ICeeGen](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md) interface pour déplacer une section.</span><span class="sxs-lookup"><span data-stu-id="e61b6-103">Represents an address offset that is used by the [ICeeGen](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md) interface to relocate a section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e61b6-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e61b6-104">Syntax</span></span>  
  
```  
typedef union  {  
    USHORT highAdj;  
} CeeSectionRelocExtra;  
```  
  
## <a name="members"></a><span data-ttu-id="e61b6-105">Membres</span><span class="sxs-lookup"><span data-stu-id="e61b6-105">Members</span></span>  
  
|<span data-ttu-id="e61b6-106">Membre</span><span class="sxs-lookup"><span data-stu-id="e61b6-106">Member</span></span>|<span data-ttu-id="e61b6-107">Description</span><span class="sxs-lookup"><span data-stu-id="e61b6-107">Description</span></span>|  
|------------|-----------------|  
|`highAdj`|<span data-ttu-id="e61b6-108">L’ajustement de la limite supérieure de la section.</span><span class="sxs-lookup"><span data-stu-id="e61b6-108">The upper address adjustment for the section.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e61b6-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e61b6-109">Requirements</span></span>  
 <span data-ttu-id="e61b6-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e61b6-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e61b6-111">**En-tête :** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e61b6-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e61b6-112">**Bibliothèque :** inclus en tant que ressource dans MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e61b6-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e61b6-113">**Versions du .NET framework :**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e61b6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e61b6-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e61b6-114">See Also</span></span>  
 [<span data-ttu-id="e61b6-115">Unions de métadonnées</span><span class="sxs-lookup"><span data-stu-id="e61b6-115">Metadata Unions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-unions.md)