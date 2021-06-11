---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339188"
---
# <a name="upmov"></a><span data-ttu-id="1adaa-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="1adaa-103">UPMOV</span></span>
 
<span data-ttu-id="1adaa-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1adaa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1adaa-105">Сведения о перемещении элементов.</span><span class="sxs-lookup"><span data-stu-id="1adaa-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="1adaa-106">Эти сведения используются во время [состояния удаления](upload-delete-status-state.md) и [состояния таблицы отправки.](upload-table-state.md)</span><span class="sxs-lookup"><span data-stu-id="1adaa-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1adaa-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="1adaa-107">Quick info</span></span>

```cpp
struct UPMOV 
{ 
      ULONG          ulFlags; 
      LPVOID         pReserved; 
      LPSTREAM       pstmReserved; 
      LPSTR          pszName; 
      FEID           feid; 
      LPMAPIFOLDER   pfld; 
      PXICC          pxicc; 
      DWORD          dwReserved; 
      PUPMOV         pupmovNext; 
      UINT           cEntMov; 
};
```

## <a name="members"></a><span data-ttu-id="1adaa-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="1adaa-108">Members</span></span>

<span data-ttu-id="1adaa-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1adaa-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1adaa-110">[in] Флаги для определения соответствующего поведения во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="1adaa-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="1adaa-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="1adaa-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="1adaa-112">[in] Проблема открытия папки сервера.</span><span class="sxs-lookup"><span data-stu-id="1adaa-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="1adaa-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="1adaa-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="1adaa-114">[in] Состояние загрузки изменилось.</span><span class="sxs-lookup"><span data-stu-id="1adaa-114">[in] The upload state has changed.</span></span> <span data-ttu-id="1adaa-115">Это используется клиентом для отслеживания изменения состояния локального магазина.</span><span class="sxs-lookup"><span data-stu-id="1adaa-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="1adaa-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="1adaa-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="1adaa-117">[in] Состояние фиксации отправки.</span><span class="sxs-lookup"><span data-stu-id="1adaa-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="1adaa-118">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="1adaa-118">_pReserved_</span></span>
  
>  <span data-ttu-id="1adaa-119">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1adaa-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="1adaa-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="1adaa-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="1adaa-121">[] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1adaa-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="1adaa-122">_pszName_</span><span class="sxs-lookup"><span data-stu-id="1adaa-122">_pszName_</span></span>
  
>  <span data-ttu-id="1adaa-123">[вышел] Имя папки назначения.</span><span class="sxs-lookup"><span data-stu-id="1adaa-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="1adaa-124">Этот член не поддерживает UNICODE.</span><span class="sxs-lookup"><span data-stu-id="1adaa-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="1adaa-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="1adaa-125">_feid_</span></span>
  
>  <span data-ttu-id="1adaa-126">[вышел] ID записи папки назначения.</span><span class="sxs-lookup"><span data-stu-id="1adaa-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="1adaa-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="1adaa-127">_pfld_</span></span>
  
>  <span data-ttu-id="1adaa-128">[in] Указатель на папку сервера.</span><span class="sxs-lookup"><span data-stu-id="1adaa-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="1adaa-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="1adaa-129">_pxicc_</span></span>
  
>  <span data-ttu-id="1adaa-130">[in] Указатель на интерфейс **контента IExchangeImportContentsChanges,** который поддерживает отправку изменений контента при использовании синхронизации инкрементных изменений (ICS).</span><span class="sxs-lookup"><span data-stu-id="1adaa-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="1adaa-131">Дополнительные сведения о **IExchangeImportContentsChanges** и ICS см. в дополнительных сведениях о [критериях оценки ICS.](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1adaa-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="1adaa-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="1adaa-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="1adaa-133">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1adaa-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="1adaa-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="1adaa-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="1adaa-135">[вышел] Следующий контекст перемещения.</span><span class="sxs-lookup"><span data-stu-id="1adaa-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="1adaa-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="1adaa-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="1adaa-137">[in] Количество перемещаемого здесь элементов.</span><span class="sxs-lookup"><span data-stu-id="1adaa-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1adaa-138">См. также</span><span class="sxs-lookup"><span data-stu-id="1adaa-138">See also</span></span>

- [<span data-ttu-id="1adaa-139">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="1adaa-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="1adaa-140">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="1adaa-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="1adaa-141">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="1adaa-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="1adaa-142">FEID</span><span class="sxs-lookup"><span data-stu-id="1adaa-142">FEID</span></span>](feid.md)

