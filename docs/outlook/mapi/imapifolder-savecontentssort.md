---
title: Имапифолдерсавеконтентссорт
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
# <a name="imapifoldersavecontentssort"></a><span data-ttu-id="36696-103">IMAPIFolder::SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="36696-103">IMAPIFolder::SaveContentsSort</span></span>

  
  
<span data-ttu-id="36696-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36696-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36696-105">Задает порядок сортировки по умолчанию для таблицы содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="36696-105">Sets the default sort order for a folder's contents table.</span></span>
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="36696-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="36696-106">Parameters</span></span>

 <span data-ttu-id="36696-107">_Лпсорткритериа_</span><span class="sxs-lookup"><span data-stu-id="36696-107">_lpSortCriteria_</span></span>
  
> <span data-ttu-id="36696-108">возврата Указатель на структуру [ссортордерсет](ssortorderset.md) , которая содержит порядок сортировки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36696-108">[in] A pointer to an [SSortOrderSet](ssortorderset.md) structure that contains the default sort order.</span></span> 
    
 <span data-ttu-id="36696-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36696-109">_ulFlags_</span></span>
  
> <span data-ttu-id="36696-110">возврата Битовая маска флагов, определяющих, как задается порядок сортировки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36696-110">[in] A bitmask of flags that controls how the default sort order is set.</span></span> <span data-ttu-id="36696-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="36696-111">The following flag can be set:</span></span>
    
<span data-ttu-id="36696-112">РЕКУРСИВЕ_СОРТ</span><span class="sxs-lookup"><span data-stu-id="36696-112">RECURSIVE_SORT</span></span> 
  
> <span data-ttu-id="36696-113">Установленный по умолчанию порядок сортировки применяется к указанной папке и ко всем вложенным папкам.</span><span class="sxs-lookup"><span data-stu-id="36696-113">The default sort order set applies to the indicated folder and to all its subfolders.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="36696-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36696-114">Return value</span></span>

<span data-ttu-id="36696-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="36696-115">S_OK</span></span> 
  
> <span data-ttu-id="36696-116">Порядок сортировки успешно сохранен.</span><span class="sxs-lookup"><span data-stu-id="36696-116">The sort order was successfully saved.</span></span>
    
<span data-ttu-id="36696-117">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="36696-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="36696-118">Поставщик хранилища сообщений не поддерживает сохранение порядка сортировки для таблиц содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="36696-118">The message store provider does not support saving a sort order for its folder contents tables.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36696-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="36696-119">Remarks</span></span>

<span data-ttu-id="36696-120">Метод **IMAPIFolder:: савеконтентссорт** устанавливает порядок сортировки по умолчанию для таблицы содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="36696-120">The **IMAPIFolder::SaveContentsSort** method establishes a default sort order for a folder's contents table.</span></span> <span data-ttu-id="36696-121">То есть когда клиент вызывает метод [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md) папки после того, как код вызывает **савеконтентссорт**, строки в таблице возвращенные содержимое будут отображаться в порядке, установленном **савеконтентссорт**.</span><span class="sxs-lookup"><span data-stu-id="36696-121">That is, when a client calls the folder's [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method after the code calls **SaveContentsSort**, the rows in the returned contents table will appear in the order established by **SaveContentsSort**.</span></span>
  
<span data-ttu-id="36696-122">Не все поставщики хранилищ сообщений поддерживают **савеконтентссорт**; поставщики хранилищ сообщений могут возвращать МАПИ_Е_НО_СУППОРТ из метода **савеконтентссорт** .</span><span class="sxs-lookup"><span data-stu-id="36696-122">Not all message store providers support **SaveContentsSort**; it is acceptable for message store providers to return MAPI_E_NO_SUPPORT from the **SaveContentsSort** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="36696-123">См. также</span><span class="sxs-lookup"><span data-stu-id="36696-123">See also</span></span>



[<span data-ttu-id="36696-124">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="36696-124">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="36696-125">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="36696-125">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="36696-126">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="36696-126">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

