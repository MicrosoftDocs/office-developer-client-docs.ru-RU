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
ms.openlocfilehash: 97575a65cd6825e07d6f11c813beec539f99f53a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436078"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="325c2-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="325c2-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="325c2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="325c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="325c2-105">Возвращает данные, необходимые для перестройки текущего свернутого или расширенного состояния классизированной таблицы.</span><span class="sxs-lookup"><span data-stu-id="325c2-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="325c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="325c2-106">Parameters</span></span>

 <span data-ttu-id="325c2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="325c2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="325c2-108">Зарезервировано; должно быть нулем.</span><span class="sxs-lookup"><span data-stu-id="325c2-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="325c2-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="325c2-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="325c2-110">[in] Количество элементов в ключе экземпляра, на которые указывает параметр _lpbInstanceKey._</span><span class="sxs-lookup"><span data-stu-id="325c2-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="325c2-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="325c2-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="325c2-112">[in] Указатель на **PR_INSTANCE_KEY** ([PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)строки, в которой необходимо перестроить текущее свернутые или расширенные состояния.</span><span class="sxs-lookup"><span data-stu-id="325c2-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="325c2-113">Параметр  _lpbInstanceKey_ не может иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="325c2-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="325c2-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="325c2-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="325c2-115">[out] Указатель на количество структур, на которые указывает параметр _lppbCollapseState._</span><span class="sxs-lookup"><span data-stu-id="325c2-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="325c2-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="325c2-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="325c2-117">[out] Указатель на указатель на структуры, содержащие данные, описывающая текущее представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="325c2-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="325c2-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="325c2-118">Return value</span></span>

<span data-ttu-id="325c2-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="325c2-119">S_OK</span></span> 
  
> <span data-ttu-id="325c2-120">Состояние классизированной таблицы успешно сохранено.</span><span class="sxs-lookup"><span data-stu-id="325c2-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="325c2-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="325c2-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="325c2-122">В настоящее время идет другая операция, которая препятствует запуску операции.</span><span class="sxs-lookup"><span data-stu-id="325c2-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="325c2-123">Либо операция должна быть завершена, либо она должна быть остановлена.</span><span class="sxs-lookup"><span data-stu-id="325c2-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="325c2-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="325c2-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="325c2-125">Таблица не поддерживает категоризации, а также расширенные и свернутые представления.</span><span class="sxs-lookup"><span data-stu-id="325c2-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="325c2-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="325c2-126">Remarks</span></span>

<span data-ttu-id="325c2-127">Метод **IMAPITable::GetCollapseState** работает с методом [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) для изменения пользовательского представления классизированной таблицы.</span><span class="sxs-lookup"><span data-stu-id="325c2-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="325c2-128">**GetCollapseState** сохраняет данные, необходимые **для SetCollapseState** для перестроения соответствующих представлений категорий классизированной таблицы.</span><span class="sxs-lookup"><span data-stu-id="325c2-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="325c2-129">Поставщики услуг определяют данные, которые необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="325c2-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="325c2-130">Однако большинство поставщиков услуг, реализующих **GetCollapseState,** сохраняет следующее:</span><span class="sxs-lookup"><span data-stu-id="325c2-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="325c2-131">Ключи сортировки (стандартные столбцы и столбцы категорий).</span><span class="sxs-lookup"><span data-stu-id="325c2-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="325c2-132">Сведения о строке, которую представляет ключ экземпляра.</span><span class="sxs-lookup"><span data-stu-id="325c2-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="325c2-133">Сведения о восстановлении свернутой и расширенной категорий таблицы.</span><span class="sxs-lookup"><span data-stu-id="325c2-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="325c2-134">Дополнительные сведения о классификации таблиц см. в таблице [сортировки и категоризации.](sorting-and-categorization.md)</span><span class="sxs-lookup"><span data-stu-id="325c2-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="325c2-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="325c2-135">Notes to implementers</span></span>

<span data-ttu-id="325c2-136">Сохранить текущее состояние всех узлов таблицы в _параметре lppbCollapseState._</span><span class="sxs-lookup"><span data-stu-id="325c2-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="325c2-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="325c2-137">Notes to callers</span></span>

<span data-ttu-id="325c2-138">Всегда **вызывай GetCollapseState** перед вызовом **SetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="325c2-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="325c2-139">См. также</span><span class="sxs-lookup"><span data-stu-id="325c2-139">See also</span></span>



[<span data-ttu-id="325c2-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="325c2-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="325c2-141">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="325c2-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

