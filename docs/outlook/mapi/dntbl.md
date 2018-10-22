---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: 'Дата последнего изменения: 05 июля 2012 г.'
ms.openlocfilehash: 4716a6f42968d7451a5db36173c4e6a9e843c08e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398124"
---
# <a name="dntbl"></a><span data-ttu-id="21142-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="21142-103">DNTBL</span></span>
 
<span data-ttu-id="21142-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21142-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21142-105">Информация для скачивания содержимого папки с сервера при [загрузке таблицы состояние](download-table-state.md) в рамках полной синхронизации содержимого хранилища.</span><span class="sxs-lookup"><span data-stu-id="21142-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="21142-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="21142-106">Quick Info</span></span>

```cpp
struct DNTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved1; 
    LPSTREAM pstmReserved2; 
    LPSTREAM pstmReserved3; 
    LPSTREAM pstmReserved4; 
    PXICC pxicc; 
    PXIHC pxihc; 
    LPSTR pszName; 
    FILETIME ftLastMod; 
    ULONG ulRights; 
    FEID feid; 
    UINT uintReserved; 
    DNTBLE rgte[2]; 
    LPSRestriction psrReserved; 
    BOOL boReserved; 
    void* pReserved1; 
    void* pReserved2; 
};

```

## <a name="members"></a><span data-ttu-id="21142-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="21142-107">Members</span></span>

<span data-ttu-id="21142-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="21142-108">_ulFlags_</span></span>
  
> <span data-ttu-id="21142-109">[in] Отмечается для изменения поведения.</span><span class="sxs-lookup"><span data-stu-id="21142-109">[in] Flags to modify behavior.</span></span> 
    
  - <span data-ttu-id="21142-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="21142-110">DNT_OK</span></span>
    
    - <span data-ttu-id="21142-111">[в] Скачивание выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="21142-111">[in] Download was successful.</span></span> <span data-ttu-id="21142-112">Устанавливается клиентом после скачивания информации с сервера.</span><span class="sxs-lookup"><span data-stu-id="21142-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="21142-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="21142-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="21142-114">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21142-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="21142-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="21142-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="21142-116">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21142-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="21142-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="21142-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="21142-118">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21142-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="21142-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="21142-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="21142-120">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21142-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="21142-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="21142-121">_pxicc_</span></span>
  
>  <span data-ttu-id="21142-122">[] Указатель для интерфейса контента **IExchangeImportContentsChanges**, который поддерживает скачивание изменений контента.</span><span class="sxs-lookup"><span data-stu-id="21142-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="21142-123">Дополнительные сведения о **IExchangeImportContentsChanges** см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="21142-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="21142-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="21142-124">_pxihc_</span></span>
  
>  <span data-ttu-id="21142-125">[out] Указатель интерфейса иерархии **IExchangeImportHierarchyChanges**, который поддерживает скачивание добавочных изменений иерархии.</span><span class="sxs-lookup"><span data-stu-id="21142-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="21142-126">Дополнительные сведения о **IExchangeImportHierarchyChanges** см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="21142-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="21142-127">_pszName_</span><span class="sxs-lookup"><span data-stu-id="21142-127">_pszName_</span></span>
  
>  <span data-ttu-id="21142-128">[out] Имя папки.</span><span class="sxs-lookup"><span data-stu-id="21142-128">Name of the folder.</span></span> 
    
<span data-ttu-id="21142-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="21142-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="21142-130">[out] Время последнего изменения папки.</span><span class="sxs-lookup"><span data-stu-id="21142-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="21142-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="21142-131">_ulRights_</span></span>
  
>  <span data-ttu-id="21142-132">[out] Значение свойства \*\* [PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx) \*\* папки.</span><span class="sxs-lookup"><span data-stu-id="21142-132">[out] Value of the **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="21142-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="21142-133">_FEID_</span></span>
  
>  <span data-ttu-id="21142-134">[out] Идентификатор записи папки.</span><span class="sxs-lookup"><span data-stu-id="21142-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="21142-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="21142-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="21142-136">[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21142-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="21142-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="21142-137">_rgte_</span></span>
  
> <span data-ttu-id="21142-138">[out] Изменения обычных (или не скрытых) и связанных (или скрытых) элементов.</span><span class="sxs-lookup"><span data-stu-id="21142-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="21142-139">*rgte [0]* – предназначено для обычных элементов, а *rgte [1]* – для связанных элементов.</span><span class="sxs-lookup"><span data-stu-id="21142-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="21142-140">Outlook заполнит значения для данного элемента во время скачивания при использовании синхронизации добавочных изменений (ICS).</span><span class="sxs-lookup"><span data-stu-id="21142-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="21142-141">Дополнительные сведения об ICS см. в статье [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="21142-141">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="21142-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="21142-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="21142-143">[in]/[out] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21142-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="21142-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="21142-144">_boReserved_</span></span>
  
>  <span data-ttu-id="21142-145">[in] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21142-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="21142-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="21142-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="21142-147">[out]Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21142-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="21142-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="21142-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="21142-149">[in] Данный элемент резервируется для внутреннего использования в Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="21142-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="21142-150">См. также</span><span class="sxs-lookup"><span data-stu-id="21142-150">See also</span></span>

- [<span data-ttu-id="21142-151">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="21142-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="21142-152">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="21142-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="21142-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="21142-153">DNTBLE</span></span>](dntble.md)

