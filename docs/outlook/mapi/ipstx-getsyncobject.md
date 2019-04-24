---
title: Ипстксжетсинкобжект
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
ms.openlocfilehash: 31ef1f5c6af498f042ab766ae90fcfbce805700a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315087"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="1cc90-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="1cc90-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="1cc90-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1cc90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1cc90-105">Запускает сеанс синхронизации и получает связанный интерфейс **[иосткс](iostxiunknown.md)** .</span><span class="sxs-lookup"><span data-stu-id="1cc90-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="1cc90-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1cc90-106">Parameters</span></span>

 <span data-ttu-id="1cc90-107">_ппосткс_</span><span class="sxs-lookup"><span data-stu-id="1cc90-107">_ppostx_</span></span>
  
>  <span data-ttu-id="1cc90-108">вышли Указатель на интерфейс **иосткс** , который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="1cc90-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1cc90-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="1cc90-109">Remarks</span></span>

<span data-ttu-id="1cc90-110">Вызывающий абонент должен гарантировать, что одна и та же папка не синхронизируется одновременно с несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="1cc90-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1cc90-111">См. также</span><span class="sxs-lookup"><span data-stu-id="1cc90-111">See also</span></span>



[<span data-ttu-id="1cc90-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="1cc90-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="1cc90-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="1cc90-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

