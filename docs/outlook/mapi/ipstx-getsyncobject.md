---
title: ипстксжетсинкобжект
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407111"
---
# <a name="ipstxgetsyncobject"></a><span data-ttu-id="89cda-103">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="89cda-103">IPSTX::GetSyncObject</span></span>

  
  
<span data-ttu-id="89cda-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89cda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89cda-105">Запускает сеанс синхронизации и получает связанный интерфейс **[иосткс](iostxiunknown.md)** .</span><span class="sxs-lookup"><span data-stu-id="89cda-105">Starts a synchronization session and gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a><span data-ttu-id="89cda-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="89cda-106">Parameters</span></span>

 <span data-ttu-id="89cda-107">_ппосткс_</span><span class="sxs-lookup"><span data-stu-id="89cda-107">_ppostx_</span></span>
  
>  <span data-ttu-id="89cda-108">вышли Указатель на интерфейс **иосткс** , который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="89cda-108">[out] Pointer to the **IOSTX** interface to get.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="89cda-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="89cda-109">Remarks</span></span>

<span data-ttu-id="89cda-110">Вызывающий абонент должен гарантировать, что одна и та же папка не синхронизируется одновременно с несколькими потоками.</span><span class="sxs-lookup"><span data-stu-id="89cda-110">The caller must ensure that the same folder is not synchronized at the same time on more than one thread.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="89cda-111">См. также</span><span class="sxs-lookup"><span data-stu-id="89cda-111">See also</span></span>



[<span data-ttu-id="89cda-112">IPSTX::EmulateSpooler</span><span class="sxs-lookup"><span data-stu-id="89cda-112">IPSTX::EmulateSpooler</span></span>](ipstx-emulatespooler.md)
  
[<span data-ttu-id="89cda-113">IPSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="89cda-113">IPSTX::GetLastError</span></span>](ipstx-getlasterror.md)

