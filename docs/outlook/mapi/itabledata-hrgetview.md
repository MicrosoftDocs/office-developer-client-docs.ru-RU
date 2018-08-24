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
ms.openlocfilehash: 0eb0374788da629c4c28eff2fce93536cf65a4ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582989"
---
# <a name="itabledatahrgetview"></a><span data-ttu-id="3daa4-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="3daa4-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="3daa4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3daa4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3daa4-105">Создание нового представления таблицы, возвращает указатель на реализацию [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="3daa4-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="3daa4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3daa4-106">Parameters</span></span>

 <span data-ttu-id="3daa4-107">_lpSSortOrderSet_</span><span class="sxs-lookup"><span data-stu-id="3daa4-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="3daa4-108">[in] Указатель на структуру порядок сортировки, который описывает порядок сортировки в табличном представлении.</span><span class="sxs-lookup"><span data-stu-id="3daa4-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="3daa4-109">Если значение NULL передается в параметре _lpSSortOrderSet_ , не сортировка.</span><span class="sxs-lookup"><span data-stu-id="3daa4-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="3daa4-110">_lpfCallerRelease_</span><span class="sxs-lookup"><span data-stu-id="3daa4-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="3daa4-111">[in] Указатель на функцию обратного вызова, на основании прототип [CALLERRELEASE](callerrelease.md) , MAPI при освобождает представления.</span><span class="sxs-lookup"><span data-stu-id="3daa4-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="3daa4-112">Если с помощью параметра _lpfCallerRelease_ передано значение NULL, функция не вызывается в выпуске представления.</span><span class="sxs-lookup"><span data-stu-id="3daa4-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="3daa4-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="3daa4-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="3daa4-114">[in] Данных, который должен быть сохранен с помощью нового представления и передается в функцию обратного вызова, на который указывает _lpfCallerRelease_.</span><span class="sxs-lookup"><span data-stu-id="3daa4-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="3daa4-115">_lppMAPITable_</span><span class="sxs-lookup"><span data-stu-id="3daa4-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="3daa4-116">[out] Указатель на указатель на только что созданный представления.</span><span class="sxs-lookup"><span data-stu-id="3daa4-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3daa4-117">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="3daa4-117">Return value</span></span>

<span data-ttu-id="3daa4-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="3daa4-118">S_OK</span></span> 
  
> <span data-ttu-id="3daa4-119">Представление успешно создан.</span><span class="sxs-lookup"><span data-stu-id="3daa4-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3daa4-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="3daa4-120">Remarks</span></span>

<span data-ttu-id="3daa4-121">Метод **ITableData::HrGetView** создает представления только для чтения данных в таблице, в порядке, на который указывает параметр _lpSSortOrderSet_ .</span><span class="sxs-lookup"><span data-stu-id="3daa4-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="3daa4-122">Курсор в начале первой строки в представлении.</span><span class="sxs-lookup"><span data-stu-id="3daa4-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="3daa4-123">Реализация интерфейса **IMAPITable** для доступа к представлении возвращается.</span><span class="sxs-lookup"><span data-stu-id="3daa4-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="3daa4-124">Поставщиков услуг вызов **HrGetView** , когда требуется предоставить клиентского доступа в таблицу.</span><span class="sxs-lookup"><span data-stu-id="3daa4-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="3daa4-125">**HrGetView** создает представление и возвращает указатель **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="3daa4-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="3daa4-126">В свою очередь, поставщиков услуг передайте указатель мыши на клиенте.</span><span class="sxs-lookup"><span data-stu-id="3daa4-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="3daa4-127">Когда клиенту по завершении работы с помощью таблицы и вызывает метод [функции IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **HrGetView** вызывает функцию обратного вызова, на который указывает параметр _lpfCallerRelease_ .</span><span class="sxs-lookup"><span data-stu-id="3daa4-127">When the client is finished using the table and calls its [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="3daa4-128">Если поставщик службы необходимо возвратить клиенту представление, набор настраиваемых столбцов или ограничение, поставщик может вызвать методы [IMAPITable::SetColumns](imapitable-setcolumns.md) и [IMAPITable::Restrict](imapitable-restrict.md) представления перед тем как разрешить клиентского доступа.</span><span class="sxs-lookup"><span data-stu-id="3daa4-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3daa4-129">См. также</span><span class="sxs-lookup"><span data-stu-id="3daa4-129">See also</span></span>



[<span data-ttu-id="3daa4-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="3daa4-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="3daa4-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3daa4-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="3daa4-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="3daa4-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="3daa4-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3daa4-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

