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
ms.openlocfilehash: 44261e5ac296004fd113d4c9123b99c482bcb732
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809573"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="23baf-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="23baf-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="23baf-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="23baf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="23baf-105">Запускает сеанс синхронизации и получает связанное интерфейс **[IOSTX](iostxiunknown.md)** .</span><span class="sxs-lookup"><span data-stu-id="23baf-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="23baf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="23baf-106">Parameters</span></span>

 <span data-ttu-id="23baf-107">_ppostx_</span><span class="sxs-lookup"><span data-stu-id="23baf-107">_ppostx_</span></span>
  
>  <span data-ttu-id="23baf-108">[out] Указатель на интерфейс **IOSTX** требуется получить.</span><span class="sxs-lookup"><span data-stu-id="23baf-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="23baf-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="23baf-109">Remarks</span></span>

<span data-ttu-id="23baf-110">Вызывающего необходимо убедиться, что и ту же папку не синхронизируются в то же время на более одного потока.</span><span class="sxs-lookup"><span data-stu-id="23baf-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23baf-111">См. также</span><span class="sxs-lookup"><span data-stu-id="23baf-111">See also</span></span>



[<span data-ttu-id="23baf-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="23baf-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="23baf-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="23baf-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

