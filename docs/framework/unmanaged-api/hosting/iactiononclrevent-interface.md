---
title: IActionOnCLREvent, interface
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IActionOnCLREvent
api_location: mscoree.dll
api_type: COM
f1_keywords: IActionOnCLREvent
helpviewer_keywords: IActionOnCLREvent interface [.NET Framework hosting]
ms.assetid: b5f9b41e-7301-429c-911f-21d5422292b3
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: eecc04fea993de3c502d1a203f0023c81c3b7909
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/21/2017
---
# <a name="iactiononclrevent-interface"></a><span data-ttu-id="54dd4-102">IActionOnCLREvent, interface</span><span class="sxs-lookup"><span data-stu-id="54dd4-102">IActionOnCLREvent Interface</span></span>
<span data-ttu-id="54dd4-103">Fournit la [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) (méthode), qui exécute des rappels sur les événements qui ont été inscrits à l’aide d’un appel à la [ICLROnEventManager::RegisterActionOnEvent](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md) (méthode).</span><span class="sxs-lookup"><span data-stu-id="54dd4-103">Provides the [IActionOnCLREvent::OnEvent](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md) method, which performs callbacks on events that have been registered by using a call to the [ICLROnEventManager::RegisterActionOnEvent](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-registeractiononevent-method.md) method.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="54dd4-104">Méthodes</span><span class="sxs-lookup"><span data-stu-id="54dd4-104">Methods</span></span>  
  
|<span data-ttu-id="54dd4-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="54dd4-105">Method</span></span>|<span data-ttu-id="54dd4-106">Description</span><span class="sxs-lookup"><span data-stu-id="54dd4-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="54dd4-107">OnEvent, méthode</span><span class="sxs-lookup"><span data-stu-id="54dd4-107">OnEvent Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iactiononclrevent-onevent-method.md)|<span data-ttu-id="54dd4-108">Exécute un rappel pour un événement enregistré.</span><span class="sxs-lookup"><span data-stu-id="54dd4-108">Performs a callback for a registered event.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="54dd4-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="54dd4-109">Requirements</span></span>  
 <span data-ttu-id="54dd4-110">**Plateformes :** consultez [requise](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="54dd4-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="54dd4-111">**En-tête :** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="54dd4-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="54dd4-112">**Bibliothèque :** inclus en tant que ressource dans MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="54dd4-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="54dd4-113">**Versions du .NET framework :**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="54dd4-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="54dd4-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54dd4-114">See Also</span></span>  
 [<span data-ttu-id="54dd4-115">EClrEvent (énumération)</span><span class="sxs-lookup"><span data-stu-id="54dd4-115">EClrEvent Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/eclrevent-enumeration.md)  
 [<span data-ttu-id="54dd4-116">ICLRControl (Interface)</span><span class="sxs-lookup"><span data-stu-id="54dd4-116">ICLRControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-interface.md)  
 [<span data-ttu-id="54dd4-117">ICLROnEventManager (Interface)</span><span class="sxs-lookup"><span data-stu-id="54dd4-117">ICLROnEventManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclroneventmanager-interface.md)  
 [<span data-ttu-id="54dd4-118">Interfaces d’hébergement</span><span class="sxs-lookup"><span data-stu-id="54dd4-118">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)