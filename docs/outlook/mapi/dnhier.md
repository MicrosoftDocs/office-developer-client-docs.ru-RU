---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Дата последнего изменения: 05 июля 2012 г.'
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389087"
---
# <a name="dnhier"></a><span data-ttu-id="31889-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="31889-103">DNHIER</span></span>

<span data-ttu-id="31889-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31889-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31889-105">Сведения о скачивании иерархии с сервера во время [загрузки состояние иерархии](download-hierarchy-state.md), которая входит в состав полной иерархии синхронизации.</span><span class="sxs-lookup"><span data-stu-id="31889-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="31889-106">Процесс скачивания использует синхронизацию добавочных изменений (ICS) Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="31889-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="31889-107">Дополнительные сведения о ICS см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="31889-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="31889-108">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="31889-108">Quick Info</span></span>

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="31889-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="31889-109">Members</span></span>

<span data-ttu-id="31889-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="31889-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="31889-111">[в] Пометки для определения соответствующего поведения во время скачивания.</span><span class="sxs-lookup"><span data-stu-id="31889-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="31889-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="31889-112">DNH_OK</span></span>
    
   - <span data-ttu-id="31889-113">[в] Скачивание выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="31889-113">[in] Download was successful.</span></span> <span data-ttu-id="31889-114">Устанавливается клиентом после скачивания информации с сервера.</span><span class="sxs-lookup"><span data-stu-id="31889-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="31889-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="31889-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="31889-116">[] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="31889-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="31889-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="31889-117">_pxihc_</span></span>
  
>  <span data-ttu-id="31889-118">[] Указатель интерфейса иерархии **IExchangeImportHierarchyChanges**, который поддерживает скачивание добавочных изменений иерархии.</span><span class="sxs-lookup"><span data-stu-id="31889-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="31889-119">Дополнительные сведения о **IExchangeImportHierarchyChanges**, см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="31889-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="31889-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="31889-120">_cEntNew_</span></span>
  
> <span data-ttu-id="31889-121">[] Количество папок, добавленных в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="31889-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="31889-122">Outlook заполнит это значение во время скачивания при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="31889-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="31889-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="31889-123">_cEntMod_</span></span>
  
> <span data-ttu-id="31889-124">[] Количество папок для изменения в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="31889-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="31889-125">Outlook заполнит это значение во время скачивания при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="31889-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="31889-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="31889-126">_cEntDel_</span></span>
  
> <span data-ttu-id="31889-127">[] Количество папок для удаления в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="31889-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="31889-128">Outlook заполнит это значение во время скачивания при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="31889-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31889-129">См. также</span><span class="sxs-lookup"><span data-stu-id="31889-129">See also</span></span>

- [<span data-ttu-id="31889-130">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="31889-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="31889-131">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="31889-131">MAPI Constants</span></span>](mapi-constants.md)

