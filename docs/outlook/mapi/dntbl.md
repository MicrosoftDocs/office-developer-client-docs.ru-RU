---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: 6096118d72dfc51fb60025a55f581ebf97b000a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808344"
---
# <a name="dntbl"></a><span data-ttu-id="c1ceb-103">DNTBL</span><span class="sxs-lookup"><span data-stu-id="c1ceb-103">DNTBL</span></span>
 
<span data-ttu-id="c1ceb-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c1ceb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c1ceb-105">Информация для загрузки содержимого папки с сервера во время, [Загрузите состояний в таблице](download-table-state.md), как часть полной синхронизации для содержимого для хранилища.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md), as part of a full synchronization for contents on a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c1ceb-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="c1ceb-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="c1ceb-107">Members</span><span class="sxs-lookup"><span data-stu-id="c1ceb-107">Members</span></span>

<span data-ttu-id="c1ceb-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-108">_ulFlags_</span></span>
  
> <span data-ttu-id="c1ceb-109">[in] Флаги для изменения поведения</span><span class="sxs-lookup"><span data-stu-id="c1ceb-109">[in] Flags to modify behavior</span></span> 
    
  - <span data-ttu-id="c1ceb-110">DNT_OK</span><span class="sxs-lookup"><span data-stu-id="c1ceb-110">DNT_OK</span></span>
    
    - <span data-ttu-id="c1ceb-111">[in] Загрузка прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-111">[in] Download was successful.</span></span> <span data-ttu-id="c1ceb-112">Клиент устанавливает это после загрузки информации с сервера.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-112">The client sets this after downloading information from the server.</span></span>
    
<span data-ttu-id="c1ceb-113">_pstmReserved1_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-113">_pstmReserved1_</span></span>
  
> <span data-ttu-id="c1ceb-114">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-114">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c1ceb-115">_pstmReserved2_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-115">_pstmReserved2_</span></span>
  
> <span data-ttu-id="c1ceb-116">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-116">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c1ceb-117">_pstmReserved3_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-117">_pstmReserved3_</span></span>
  
> <span data-ttu-id="c1ceb-118">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-118">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c1ceb-119">_pstmReserved4_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-119">_pstmReserved4_</span></span>
  
> <span data-ttu-id="c1ceb-120">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-120">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c1ceb-121">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-121">_pxicc_</span></span>
  
>  <span data-ttu-id="c1ceb-122">[out] Указатель на интерфейс **IExchangeImportContentsChanges** содержимое, которое поддерживает загрузки содержимого изменений.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-122">[out] Pointer to the **IExchangeImportContentsChanges** contents interface that supports downloading content changes.</span></span> <span data-ttu-id="c1ceb-123">Дополнительные сведения о **IExchangeImportContentsChanges** [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-123">For more information on **IExchangeImportContentsChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="c1ceb-124">_pxihc_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-124">_pxihc_</span></span>
  
>  <span data-ttu-id="c1ceb-125">[out] Указатель на интерфейс **IExchangeImportHierarchyChanges** иерархии, которая поддерживает загрузки изменений добавочного иерархии.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-125">[out] Pointer to the **IExchangeImportHierarchyChanges** hierarchy interface that supports downloading incremental hierarchy changes.</span></span> <span data-ttu-id="c1ceb-126">Дополнительные сведения о **IExchangeImportHierarchyChanges** [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-126">For more information on **IExchangeImportHierarchyChanges**, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="c1ceb-127">_параметра pszName_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-127">_pszName_</span></span>
  
>  <span data-ttu-id="c1ceb-128">[out] Имя папки.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-128">[out] Name of the folder.</span></span> 
    
<span data-ttu-id="c1ceb-129">_ftLastMod_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-129">_ftLastMod_</span></span>
  
>  <span data-ttu-id="c1ceb-130">[out] Время последнего изменения папки.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-130">[out] Last modification time of the folder.</span></span> 
    
<span data-ttu-id="c1ceb-131">_ulRights_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-131">_ulRights_</span></span>
  
>  <span data-ttu-id="c1ceb-132">[out] Значение свойства **[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** папки.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-132">[out] Value of the **[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** property of the folder.</span></span> 
    
<span data-ttu-id="c1ceb-133">_feid_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-133">_feid_</span></span>
  
>  <span data-ttu-id="c1ceb-134">[out] Идентификатор записи папки.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-134">[out] Entry ID of the folder.</span></span> 
    
<span data-ttu-id="c1ceb-135">_uintReserved_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-135">_uintReserved_</span></span>
  
>  <span data-ttu-id="c1ceb-136">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-136">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c1ceb-137">_rgte_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-137">_rgte_</span></span>
  
> <span data-ttu-id="c1ceb-138">[out] Изменения для обычного (или не скрыты) и связанные (или скрытых) элементов.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-138">[out] Changes for normal (or non-hidden) and associated (or hidden) items.</span></span>  <span data-ttu-id="c1ceb-139">*rgte [0]* — это для обычных элементов и *rgte [1]* — это для связанных элементов.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-139">*rgte[0]*  is for normal items, and  *rgte[1]*  is for associated items.</span></span> <span data-ttu-id="c1ceb-140">Этот член заполняет Outlook во время загрузки при использовании добавочной синхронизации изменений (ICS).</span><span class="sxs-lookup"><span data-stu-id="c1ceb-140">Outlook populates this member during the downloading when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="c1ceb-141">Дополнительные сведения о ICS [Критерии оценки ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-141">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="c1ceb-142">_lpsrReserved_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-142">_lpsrReserved_</span></span>
  
>  <span data-ttu-id="c1ceb-143">[в] и [out] этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-143">[in]/[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c1ceb-144">_boReserved_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-144">_boReserved_</span></span>
  
>  <span data-ttu-id="c1ceb-145">[in] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-145">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c1ceb-146">_pReserved1_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-146">_pReserved1_</span></span>
  
>  <span data-ttu-id="c1ceb-147">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-147">[out]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="c1ceb-148">_pReserved2_</span><span class="sxs-lookup"><span data-stu-id="c1ceb-148">_pReserved2_</span></span>
  
>  <span data-ttu-id="c1ceb-149">[in] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1ceb-149">[in]This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c1ceb-150">См. также</span><span class="sxs-lookup"><span data-stu-id="c1ceb-150">See also</span></span>

- [<span data-ttu-id="c1ceb-151">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="c1ceb-151">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)  
- [<span data-ttu-id="c1ceb-152">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="c1ceb-152">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="c1ceb-153">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="c1ceb-153">DNTBLE</span></span>](dntble.md)

