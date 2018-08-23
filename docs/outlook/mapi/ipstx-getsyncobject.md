---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e0e27d86098ec55849fa96cc150c60934ef2810b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585453"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="03f8b-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="03f8b-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="03f8b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03f8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03f8b-105">Запускает сеанс синхронизации и получает связанное интерфейс **[IOSTX](iostxiunknown.md)** .</span><span class="sxs-lookup"><span data-stu-id="03f8b-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="03f8b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="03f8b-106">Parameters</span></span>

 <span data-ttu-id="03f8b-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="03f8b-107">_ppostx_</span></span>
  
>  <span data-ttu-id="03f8b-108">[out] Указатель на интерфейс **IOSTX** требуется получить.</span><span class="sxs-lookup"><span data-stu-id="03f8b-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="03f8b-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="03f8b-109">Remarks</span></span>

<span data-ttu-id="03f8b-110">Вызывающего необходимо убедиться, что и ту же папку не синхронизируются в то же время на более одного потока.</span><span class="sxs-lookup"><span data-stu-id="03f8b-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="03f8b-111">См. также</span><span class="sxs-lookup"><span data-stu-id="03f8b-111">See also</span></span>



[<span data-ttu-id="03f8b-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="03f8b-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="03f8b-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="03f8b-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

