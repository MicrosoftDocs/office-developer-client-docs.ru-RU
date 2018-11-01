---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 46d993060d03b8c22c2d6c083c05f023648e6642
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589667"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="5611f-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="5611f-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="5611f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5611f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5611f-105">Возвращает данные, необходимые для перестроения текущего свернут или развернут состояние форматирование таблицы.</span><span class="sxs-lookup"><span data-stu-id="5611f-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="5611f-106">���������</span><span class="sxs-lookup"><span data-stu-id="5611f-106">Parameters</span></span>

 <span data-ttu-id="5611f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5611f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5611f-108">Зарезервировано; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="5611f-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="5611f-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="5611f-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="5611f-110">[in] Число байт в экземпляре ключ, на который указывает параметр _lpbInstanceKey_ .</span><span class="sxs-lookup"><span data-stu-id="5611f-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="5611f-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="5611f-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="5611f-112">[in] Указатель на **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) свойство строки, в которой текущего свернут или развернут состояние следует перестроение.</span><span class="sxs-lookup"><span data-stu-id="5611f-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="5611f-113">Параметр _lpbInstanceKey_ не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="5611f-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="5611f-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="5611f-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="5611f-115">[out] Указатель на число указывает параметр _lppbCollapseState_ структуры.</span><span class="sxs-lookup"><span data-stu-id="5611f-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="5611f-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="5611f-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="5611f-117">[out] Указатель на указатель на структуры, содержащие данные, которые описывают текущее представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="5611f-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5611f-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5611f-118">Return value</span></span>

<span data-ttu-id="5611f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="5611f-119">S_OK</span></span> 
  
> <span data-ttu-id="5611f-120">Состояние для форматирование таблицы успешно сохранен.</span><span class="sxs-lookup"><span data-stu-id="5611f-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="5611f-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="5611f-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="5611f-122">В, не позволяющей операция запуск выполняется другой операции.</span><span class="sxs-lookup"><span data-stu-id="5611f-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="5611f-123">В процессе выполнения операции должны выполнить либо должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="5611f-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="5611f-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5611f-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5611f-125">Таблица не поддерживает категоризации и дополненная и сжатого представления.</span><span class="sxs-lookup"><span data-stu-id="5611f-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5611f-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="5611f-126">Remarks</span></span>

<span data-ttu-id="5611f-127">Метод **IMAPITable::GetCollapseState** работает с помощью метода [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) для изменения представления пользователя по категориям таблицы.</span><span class="sxs-lookup"><span data-stu-id="5611f-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="5611f-128">**GetCollapseState** сохраняет данные, необходимые для **SetCollapseState** для использования для перестроения соответствующих представлений категорий форматирование таблицы.</span><span class="sxs-lookup"><span data-stu-id="5611f-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="5611f-129">Сохранение данных определите, поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="5611f-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="5611f-130">Тем не менее большинство поставщиков услуг, реализация **GetCollapseState** сохраните следующее:</span><span class="sxs-lookup"><span data-stu-id="5611f-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="5611f-131">Ключи сортировки (стандартный столбцов и столбцов категории).</span><span class="sxs-lookup"><span data-stu-id="5611f-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="5611f-132">Сведения о строку, представляющую ключ экземпляра.</span><span class="sxs-lookup"><span data-stu-id="5611f-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="5611f-133">Сведения для восстановления категорий свернутые и улучшенные таблицы.</span><span class="sxs-lookup"><span data-stu-id="5611f-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="5611f-134">Дополнительные сведения о таблицах по категориям можно [Сортировка и классификации](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="5611f-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5611f-135">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="5611f-135">Notes to implementers</span></span>

<span data-ttu-id="5611f-136">Хранить текущее состояние всех узлов таблицы с помощью параметра _lppbCollapseState_ .</span><span class="sxs-lookup"><span data-stu-id="5611f-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5611f-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="5611f-137">Notes to callers</span></span>

<span data-ttu-id="5611f-138">Всегда вызовите **GetCollapseState** перед вызовом **SetCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="5611f-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5611f-139">См. также</span><span class="sxs-lookup"><span data-stu-id="5611f-139">See also</span></span>



[<span data-ttu-id="5611f-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="5611f-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="5611f-141">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5611f-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

