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
ms.openlocfilehash: 7c8ccada96b3e34372d488e16c85627e8b6b0cd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808869"
---
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="a5d66-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="a5d66-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="a5d66-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a5d66-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a5d66-105">Задает порядок сортировки по умолчанию для папки содержимое таблицы.</span><span class="sxs-lookup"><span data-stu-id="a5d66-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a5d66-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5d66-106">Parameters</span></span>

 <span data-ttu-id="a5d66-107">_lpSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="a5d66-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="a5d66-108">[in] Указатель на структуру [SSortOrderSet](ssortorderset.md) , содержащий порядок сортировки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5d66-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="a5d66-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a5d66-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a5d66-110">[in] Битовая маска флаги, который определяет, как задать порядок сортировки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a5d66-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="a5d66-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a5d66-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a5d66-112">RECURSIVE_SORT</span><span class="sxs-lookup"><span data-stu-id="a5d66-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="a5d66-113">Набор порядок сортировки по умолчанию применяется для указанной папки и все вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="a5d66-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5d66-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4">Return value</span></span>

<span data-ttu-id="a5d66-115">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="a5d66-115">S_OK</span></span> 
  
> <span data-ttu-id="a5d66-116">Порядок сортировки успешно сохранен.</span><span class="sxs-lookup"><span data-stu-id="a5d66-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="a5d66-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a5d66-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a5d66-118">Поставщик хранения сообщения не поддерживает сохранение порядок сортировки для своих таблиц содержимое папки.</span><span class="sxs-lookup"><span data-stu-id="a5d66-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5d66-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="a5d66-119">Remarks</span></span>

<span data-ttu-id="a5d66-120">Метод **IMAPIFolder::SaveContentsSort** устанавливает порядок сортировки по умолчанию для папки содержимое таблицы.</span><span class="sxs-lookup"><span data-stu-id="a5d66-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="a5d66-121">То есть когда клиент вызывает метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) папки после код вызывает **SaveContentsSort**, строки в таблице возвращаемых содержимое отображаются в порядке, установленные **SaveContentsSort**.</span><span class="sxs-lookup"><span data-stu-id="a5d66-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="a5d66-122">Не все поставщики хранилища сообщений поддерживают **SaveContentsSort**; Это допустимо для поставщиков хранилища сообщений для возврата MAPI_E_NO_SUPPORT из метода **SaveContentsSort** .</span><span class="sxs-lookup"><span data-stu-id="a5d66-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a5d66-123">См. также</span><span class="sxs-lookup"><span data-stu-id="a5d66-123">See also</span></span>



[<span data-ttu-id="a5d66-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="a5d66-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="a5d66-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="a5d66-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="a5d66-126">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a5d66-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

