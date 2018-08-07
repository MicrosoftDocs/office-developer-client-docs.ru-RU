---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: 3c7d59849fcd66a5fe90623b7bb8516d13b4a2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808345"
---
# <a name="dnhier"></a><span data-ttu-id="61634-103">DNHIER</span><span class="sxs-lookup"><span data-stu-id="61634-103">DNHIER</span></span>

<span data-ttu-id="61634-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61634-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61634-105">Сведения для загрузки иерархии с сервера во время, [Загрузите иерархия состояний](download-hierarchy-state.md), которая является частью полную иерархию синхронизации.</span><span class="sxs-lookup"><span data-stu-id="61634-105">Information for downloading a hierarchy from the server during the [download hierarchy state](download-hierarchy-state.md), which is part of a full hierarchy synchronization.</span></span> <span data-ttu-id="61634-106">Этот процесс загрузки использует Microsoft Exchange добавочные изменения синхронизации (ICS).</span><span class="sxs-lookup"><span data-stu-id="61634-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="61634-107">Дополнительные сведения о ICS [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="61634-107">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="61634-108">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="61634-108">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="61634-109">Members</span><span class="sxs-lookup"><span data-stu-id="61634-109">Members</span></span>

<span data-ttu-id="61634-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="61634-110">_ulFlags_</span></span>
  
>  <span data-ttu-id="61634-111">[in] Флаги для определения соответствующего поведения во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="61634-111">[in] Flags to determine the appropriate behavior during the download.</span></span> 
    
   - <span data-ttu-id="61634-112">DNH_OK</span><span class="sxs-lookup"><span data-stu-id="61634-112">DNH_OK</span></span>
    
   - <span data-ttu-id="61634-113">[in] Загрузка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="61634-113">[in] Download was successful.</span></span> <span data-ttu-id="61634-114">Клиент устанавливает это после загрузки информации с сервера.</span><span class="sxs-lookup"><span data-stu-id="61634-114">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="61634-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="61634-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="61634-116">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="61634-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="61634-117">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="61634-117">_pxihc_</span></span>
  
>  <span data-ttu-id="61634-118">[out] Указатель на интерфейс **IExchangeImportHierarchyChanges** иерархии, которая поддерживает загрузки изменений добавочного иерархии.</span><span class="sxs-lookup"><span data-stu-id="61634-118">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="61634-119">Дополнительные сведения о **IExchangeImportHierarchyChanges** [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="61634-119">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="61634-120">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="61634-120">_cEntNew_</span></span>
  
> <span data-ttu-id="61634-121">[out] Число папки, добавленные в локальном хранилище.</span><span class="sxs-lookup"><span data-stu-id="61634-121">[out] Number of folders added to the local store.</span></span> <span data-ttu-id="61634-122">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="61634-122">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="61634-123">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="61634-123">_cEntMod_</span></span>
  
> <span data-ttu-id="61634-124">[out] Число папок, которые следует изменить для локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="61634-124">[out] Number of folders to be modified on the local store.</span></span> <span data-ttu-id="61634-125">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="61634-125">Outlook populates this value during the downloading when using ICS.</span></span>
    
<span data-ttu-id="61634-126">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="61634-126">_cEntDel_</span></span>
  
> <span data-ttu-id="61634-127">[out] Число папок к удалению локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="61634-127">[out] Number of folders to be deleted on the local store.</span></span> <span data-ttu-id="61634-128">Outlook заполняет это значение во время загрузки при использовании ICS.</span><span class="sxs-lookup"><span data-stu-id="61634-128">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61634-129">См. также</span><span class="sxs-lookup"><span data-stu-id="61634-129">See also</span></span>

- [<span data-ttu-id="61634-130">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="61634-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md) 
- [<span data-ttu-id="61634-131">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="61634-131">MAPI Constants</span></span>](mapi-constants.md)

