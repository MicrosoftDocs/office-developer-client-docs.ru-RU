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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393385"
---
# <a name="upmov"></a><span data-ttu-id="7dd7c-103">UPMOV</span><span class="sxs-lookup"><span data-stu-id="7dd7c-103">UPMOV</span></span>
 
<span data-ttu-id="7dd7c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dd7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dd7c-105">Информация для загрузки элементов, которые были перемещены.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-105">Information for uploading items that have been moved.</span></span> <span data-ttu-id="7dd7c-106">Эти сведения используются во время [загрузки удалить состояние состояния](upload-delete-status-state.md) и [Отправка состояний в таблице](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="7dd7c-106">This information is used during the [upload delete status state](upload-delete-status-state.md) and [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7dd7c-107">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="7dd7c-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="7dd7c-108">Members</span><span class="sxs-lookup"><span data-stu-id="7dd7c-108">Members</span></span>

<span data-ttu-id="7dd7c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7dd7c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="7dd7c-110">[in] Флаги для определения соответствующего поведения во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-110">[in] Flags to determine the appropriate behavior during the upload.</span></span>
    
  - <span data-ttu-id="7dd7c-111">UPV_ERROR</span><span class="sxs-lookup"><span data-stu-id="7dd7c-111">UPV_ERROR</span></span>
    
    - <span data-ttu-id="7dd7c-112">[in] Ошибка при открытии папки на сервере.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-112">[in] Problem opening server folder.</span></span>
    
  - <span data-ttu-id="7dd7c-113">UPV_DIRTY</span><span class="sxs-lookup"><span data-stu-id="7dd7c-113">UPV_DIRTY</span></span>
    
    - <span data-ttu-id="7dd7c-114">[in] Отправить состояние изменилось.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-114">[in] The upload state has changed.</span></span> <span data-ttu-id="7dd7c-115">Используется клиентом для отслеживания изменений в состоянии для локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-115">This is used by the client to track the change in state for the local store.</span></span>
    
  - <span data-ttu-id="7dd7c-116">UPV_COMMIT</span><span class="sxs-lookup"><span data-stu-id="7dd7c-116">UPV_COMMIT</span></span>
    
    - <span data-ttu-id="7dd7c-117">[in] Сохранить состояние передачи.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-117">[in] Commit upload state.</span></span>
    
<span data-ttu-id="7dd7c-118">_Сохраняются_</span><span class="sxs-lookup"><span data-stu-id="7dd7c-118">_pReserved_</span></span>
  
>  <span data-ttu-id="7dd7c-119">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-119">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7dd7c-120">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="7dd7c-120">_pstmReserved_</span></span>
  
>  <span data-ttu-id="7dd7c-121">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-121">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7dd7c-122">_параметра pszName_</span><span class="sxs-lookup"><span data-stu-id="7dd7c-122">_pszName_</span></span>
  
>  <span data-ttu-id="7dd7c-123">[out] Имя папки назначения.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-123">[out] Name of the destination folder.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="7dd7c-124">Этот член не поддерживает Юникод.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-124">This member does not support UNICODE.</span></span> 
  
<span data-ttu-id="7dd7c-125">_feid_</span><span class="sxs-lookup"><span data-stu-id="7dd7c-125">_feid_</span></span>
  
>  <span data-ttu-id="7dd7c-126">[out] Идентификатор записи папки назначения.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-126">[out] Entry ID of destination folder.</span></span> 
    
<span data-ttu-id="7dd7c-127">_pfld_</span><span class="sxs-lookup"><span data-stu-id="7dd7c-127">_pfld_</span></span>
  
>  <span data-ttu-id="7dd7c-128">[in] Указатель на папку сервера.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-128">[in] Pointer to server folder.</span></span> 
    
<span data-ttu-id="7dd7c-129">_pxicc_</span><span class="sxs-lookup"><span data-stu-id="7dd7c-129">_pxicc_</span></span>
  
>  <span data-ttu-id="7dd7c-130">[in] Указатель на интерфейс **IExchangeImportContentsChanges** содержимое, которое поддерживает отправки контента изменений при использовании добавочной синхронизации изменений (ICS).</span><span class="sxs-lookup"><span data-stu-id="7dd7c-130">[in] Pointer to the **IExchangeImportContentsChanges** contents interface that supports uploading content changes when using Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="7dd7c-131">Дополнительные сведения о **IExchangeImportContentsChanges** и ICS [Критерии оценки ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)см.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-131">For more information on **IExchangeImportContentsChanges** and ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
    
<span data-ttu-id="7dd7c-132">_dwReserved_</span><span class="sxs-lookup"><span data-stu-id="7dd7c-132">_dwReserved_</span></span>
  
>  <span data-ttu-id="7dd7c-133">[out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-133">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="7dd7c-134">_pupmovNext_</span><span class="sxs-lookup"><span data-stu-id="7dd7c-134">_pupmovNext_</span></span>
  
>  <span data-ttu-id="7dd7c-135">[out] Далее перемещение контекста.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-135">[out] Next move context.</span></span> 
    
<span data-ttu-id="7dd7c-136">_cEntMov_</span><span class="sxs-lookup"><span data-stu-id="7dd7c-136">_cEntMov_</span></span>
  
>  <span data-ttu-id="7dd7c-137">[in] Количество элементов Переместить сюда.</span><span class="sxs-lookup"><span data-stu-id="7dd7c-137">[in] Number of items moved here.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7dd7c-138">См. также</span><span class="sxs-lookup"><span data-stu-id="7dd7c-138">See also</span></span>

- [<span data-ttu-id="7dd7c-139">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="7dd7c-139">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="7dd7c-140">Сведения о конечном автомате репликации</span><span class="sxs-lookup"><span data-stu-id="7dd7c-140">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="7dd7c-141">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="7dd7c-141">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="7dd7c-142">FEID</span><span class="sxs-lookup"><span data-stu-id="7dd7c-142">FEID</span></span>](feid.md)

