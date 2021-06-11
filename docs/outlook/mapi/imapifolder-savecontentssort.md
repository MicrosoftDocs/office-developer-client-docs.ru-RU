---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c142424bb050ae287f54a87ea8a5e0ea45acb12c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411619"
---
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="dcf39-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="dcf39-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="dcf39-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dcf39-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dcf39-105">Задает порядок сортировки по умолчанию для таблицы содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="dcf39-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="dcf39-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="dcf39-106">Parameters</span></span>

 <span data-ttu-id="dcf39-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="dcf39-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="dcf39-108">[in] Указатель на структуру [SSortOrderSet,](ssortorderset.md) которая содержит порядок сортировки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dcf39-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="dcf39-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dcf39-109">_ulFlags_</span></span>
  
> <span data-ttu-id="dcf39-110">[in] Битмашка флагов, которые контролируют, как установлен порядок сортировки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dcf39-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="dcf39-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="dcf39-111">The following flag can be set:</span></span>
    
<span data-ttu-id="dcf39-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="dcf39-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="dcf39-113">Набор сортировки по умолчанию применяется к указанным папкам и ко всем ее подмосткам.</span><span class="sxs-lookup"><span data-stu-id="dcf39-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dcf39-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcf39-114">Return value</span></span>

<span data-ttu-id="dcf39-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="dcf39-115">S_OK</span></span> 
  
> <span data-ttu-id="dcf39-116">Порядок сортировки был успешно сохранен.</span><span class="sxs-lookup"><span data-stu-id="dcf39-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="dcf39-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="dcf39-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="dcf39-118">Поставщик хранения сообщений не поддерживает сохранение порядка сортировки для таблиц содержимого папок.</span><span class="sxs-lookup"><span data-stu-id="dcf39-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dcf39-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="dcf39-119">Remarks</span></span>

<span data-ttu-id="dcf39-120">Метод **IMAPIFolder::SaveContentsSort** устанавливает порядок сортировки по умолчанию для таблицы содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="dcf39-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="dcf39-121">То есть, когда клиент вызывает метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) после вызова кода **SaveContentsSort,** строки в таблице возвращаемого контента будут отображаться в порядке, установленном **SaveContentsSort.**</span><span class="sxs-lookup"><span data-stu-id="dcf39-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="dcf39-122">Не все поставщики магазинов сообщений поддерживают **SaveContentsSort;** допустимо, чтобы поставщики хранения сообщений возвращали MAPI_E_NO_SUPPORT из **метода SaveContentsSort.**</span><span class="sxs-lookup"><span data-stu-id="dcf39-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dcf39-123">См. также</span><span class="sxs-lookup"><span data-stu-id="dcf39-123">See also</span></span>



[<span data-ttu-id="dcf39-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="dcf39-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="dcf39-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="dcf39-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="dcf39-126">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="dcf39-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

