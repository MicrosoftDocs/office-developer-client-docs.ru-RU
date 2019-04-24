---
title: Имапитаблежетколлапсестате
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328930"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="d3a27-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="d3a27-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="d3a27-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3a27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3a27-105">Возвращает данные, необходимые для перестроения текущего свернутого или развернутого состояния таблицы с классификацией.</span><span class="sxs-lookup"><span data-stu-id="d3a27-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="d3a27-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d3a27-106">Parameters</span></span>

 <span data-ttu-id="d3a27-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d3a27-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d3a27-108">Резервирования должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d3a27-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d3a27-109">_Кбинстанцекэй_</span><span class="sxs-lookup"><span data-stu-id="d3a27-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="d3a27-110">возврата Количество байтов в ключе экземпляра, на которое указывает параметр _лпбинстанцекэй_ .</span><span class="sxs-lookup"><span data-stu-id="d3a27-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="d3a27-111">_Лпбинстанцекэй_</span><span class="sxs-lookup"><span data-stu-id="d3a27-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="d3a27-112">возврата Указатель на свойство **пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) строки, в которой должно быть перестроено текущее свернутое или развернутое состояние.</span><span class="sxs-lookup"><span data-stu-id="d3a27-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="d3a27-113">Параметр _лпбинстанцекэй_ не может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="d3a27-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="d3a27-114">_Лпкбколлапсестате_</span><span class="sxs-lookup"><span data-stu-id="d3a27-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="d3a27-115">вышли Указатель на число структур, на которые указывает параметр _лппбколлапсестате_ .</span><span class="sxs-lookup"><span data-stu-id="d3a27-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="d3a27-116">_Лппбколлапсестате_</span><span class="sxs-lookup"><span data-stu-id="d3a27-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="d3a27-117">вышли Указатель на указатель на структуры, содержащие данные, описывающие текущее представление таблицы.</span><span class="sxs-lookup"><span data-stu-id="d3a27-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d3a27-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d3a27-118">Return value</span></span>

<span data-ttu-id="d3a27-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3a27-119">S_OK</span></span> 
  
> <span data-ttu-id="d3a27-120">Состояние таблицы с классификацией успешно сохранено.</span><span class="sxs-lookup"><span data-stu-id="d3a27-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="d3a27-121">МАПИ_Е_БУСИ</span><span class="sxs-lookup"><span data-stu-id="d3a27-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="d3a27-122">Выполняется другая операция, которая не позволяет запустить операцию.</span><span class="sxs-lookup"><span data-stu-id="d3a27-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="d3a27-123">Выполнение выполняемой операции должно быть разрешено или остановлено.</span><span class="sxs-lookup"><span data-stu-id="d3a27-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="d3a27-124">МАПИ_Е_НО_СУППОРТ</span><span class="sxs-lookup"><span data-stu-id="d3a27-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d3a27-125">В таблице не поддерживаются категоризация и развернутые и свернутые представления.</span><span class="sxs-lookup"><span data-stu-id="d3a27-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d3a27-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d3a27-126">Remarks</span></span>

<span data-ttu-id="d3a27-127">Метод **IMAPITable:: жетколлапсестате** работает с методом [IMAPITable:: сетколлапсестате](imapitable-setcollapsestate.md) для изменения пользовательского представления таблицы с классификацией.</span><span class="sxs-lookup"><span data-stu-id="d3a27-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="d3a27-128">**Жетколлапсестате** сохраняет данные, необходимые для использования **сетколлапсестате** , для перестроения соответствующих представлений категорий таблицы с классификацией.</span><span class="sxs-lookup"><span data-stu-id="d3a27-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="d3a27-129">Поставщики услуг определяют данные, которые необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="d3a27-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="d3a27-130">Однако большинство поставщиков услуг, реализующих **жетколлапсестате** , сохраняют следующие данные:</span><span class="sxs-lookup"><span data-stu-id="d3a27-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="d3a27-131">Ключи сортировки (столбцы стандартных столбцов и категорий).</span><span class="sxs-lookup"><span data-stu-id="d3a27-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="d3a27-132">Сведения о строке, которую представляет ключ экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d3a27-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="d3a27-133">Сведения для восстановления свернутых и развернутых категорий таблицы.</span><span class="sxs-lookup"><span data-stu-id="d3a27-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="d3a27-134">Для получения дополнительных сведений об классифицированных таблицах, ознакомьтесь со статьей [Сортировка и категоризация](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="d3a27-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d3a27-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d3a27-135">Notes to implementers</span></span>

<span data-ttu-id="d3a27-136">Сохраните текущее состояние всех узлов таблицы в параметре _лппбколлапсестате_ .</span><span class="sxs-lookup"><span data-stu-id="d3a27-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d3a27-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d3a27-137">Notes to callers</span></span>

<span data-ttu-id="d3a27-138">Всегда вызывайте **жетколлапсестате** перед вызовом **сетколлапсестате**.</span><span class="sxs-lookup"><span data-stu-id="d3a27-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d3a27-139">См. также</span><span class="sxs-lookup"><span data-stu-id="d3a27-139">See also</span></span>



[<span data-ttu-id="d3a27-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="d3a27-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="d3a27-141">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d3a27-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

