---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278717"
---
# <a name="itabledatahrgetview"></a><span data-ttu-id="aceb4-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="aceb4-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="aceb4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aceb4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aceb4-105">Создает представление таблицы, возвращая указатель в [реализацию IMAPITable.](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="aceb4-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="aceb4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="aceb4-106">Parameters</span></span>

 <span data-ttu-id="aceb4-107">_lpSSortOrderSet_</span><span class="sxs-lookup"><span data-stu-id="aceb4-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="aceb4-108">[in] Указатель на структуру порядка сортировки, которая описывает порядок сортировки для представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="aceb4-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="aceb4-109">Если NULL передается в  _параметре lpSSortOrderSet,_ представление не сортироваться.</span><span class="sxs-lookup"><span data-stu-id="aceb4-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="aceb4-110">_lpfCallerRelease_</span><span class="sxs-lookup"><span data-stu-id="aceb4-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="aceb4-111">[in] Указатель на функцию вызова на основе прототипа [CALLERRELEASE,](callerrelease.md) вызываемого MAPI при выпуске представления.</span><span class="sxs-lookup"><span data-stu-id="aceb4-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="aceb4-112">Если NULL передается в  _параметре lpfCallerRelease,_ при выпуске представления функция не называется.</span><span class="sxs-lookup"><span data-stu-id="aceb4-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="aceb4-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="aceb4-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="aceb4-114">[in] Данные, которые необходимо сохранить с помощью нового представления и передать функции вызова, на которые указывает _lpfCallerRelease._</span><span class="sxs-lookup"><span data-stu-id="aceb4-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="aceb4-115">_lppMAPITable_</span><span class="sxs-lookup"><span data-stu-id="aceb4-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="aceb4-116">[вышел] Указатель на указатель на вновь созданное представление.</span><span class="sxs-lookup"><span data-stu-id="aceb4-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="aceb4-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aceb4-117">Return value</span></span>

<span data-ttu-id="aceb4-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="aceb4-118">S_OK</span></span> 
  
> <span data-ttu-id="aceb4-119">Представление было успешно создано.</span><span class="sxs-lookup"><span data-stu-id="aceb4-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aceb4-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="aceb4-120">Remarks</span></span>

<span data-ttu-id="aceb4-121">Метод **ITableData::HrGetView** создает представление данных в таблице только для чтения, отсортировали в порядке, указываемом параметром _lpSSortOrderSet._</span><span class="sxs-lookup"><span data-stu-id="aceb4-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="aceb4-122">Курсор помещается в начале первой строки в представлении.</span><span class="sxs-lookup"><span data-stu-id="aceb4-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="aceb4-123">Возвращается реализация интерфейса **IMAPITable** для доступа к представлению.</span><span class="sxs-lookup"><span data-stu-id="aceb4-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="aceb4-124">Поставщики услуг **звонят в HrGetView,** когда им необходимо предоставить клиенту доступ к таблице.</span><span class="sxs-lookup"><span data-stu-id="aceb4-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="aceb4-125">**HrGetView** создает представление и возвращает **указатель IMAPITable.**</span><span class="sxs-lookup"><span data-stu-id="aceb4-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="aceb4-126">Поставщики услуг в свою очередь передают указатель клиенту.</span><span class="sxs-lookup"><span data-stu-id="aceb4-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="aceb4-127">Когда клиент заканчивает использовать таблицу и вызывает метод [IUnknown::Release,](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) **HrGetView** вызывает функцию вызова, отмеченную параметром _lpfCallerRelease._</span><span class="sxs-lookup"><span data-stu-id="aceb4-127">When the client is finished using the table and calls its [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="aceb4-128">Если поставщику услуг необходимо вернуть клиенту представление с настраиваемым набором столбцов или ограничением, перед разрешением клиентского доступа поставщик может вызвать [IMAPITable::SetColumns](imapitable-setcolumns.md) и [IMAPITable::Restrict.](imapitable-restrict.md)</span><span class="sxs-lookup"><span data-stu-id="aceb4-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aceb4-129">См. также</span><span class="sxs-lookup"><span data-stu-id="aceb4-129">See also</span></span>



[<span data-ttu-id="aceb4-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="aceb4-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="aceb4-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aceb4-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="aceb4-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="aceb4-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="aceb4-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aceb4-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

