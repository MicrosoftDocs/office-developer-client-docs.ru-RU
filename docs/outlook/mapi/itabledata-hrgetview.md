---
title: итабледатахржетвиев
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
# <a name="itabledatahrgetview"></a><span data-ttu-id="ae1e2-103">ITableData::HrGetView</span><span class="sxs-lookup"><span data-stu-id="ae1e2-103">ITableData::HrGetView</span></span>

  
  
<span data-ttu-id="ae1e2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae1e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae1e2-105">Создает табличное представление, возвращая указатель на реализацию [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="ae1e2-105">Creates a table view, returning a pointer to an [IMAPITable](imapitableiunknown.md) implementation.</span></span> 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a><span data-ttu-id="ae1e2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae1e2-106">Parameters</span></span>

 <span data-ttu-id="ae1e2-107">_лпссортордерсет_</span><span class="sxs-lookup"><span data-stu-id="ae1e2-107">_lpSSortOrderSet_</span></span>
  
> <span data-ttu-id="ae1e2-108">возврата Указатель на структуру порядка сортировки, в которой описывается порядок сортировки для представления таблицы.</span><span class="sxs-lookup"><span data-stu-id="ae1e2-108">[in] A pointer to a sort order structure that describes the sort order for the table view.</span></span> <span data-ttu-id="ae1e2-109">Если в параметре _лпссортордерсет_ передается значение null, представление не сортируется.</span><span class="sxs-lookup"><span data-stu-id="ae1e2-109">If NULL is passed in the  _lpSSortOrderSet_ parameter, the view is not sorted.</span></span> 
    
 <span data-ttu-id="ae1e2-110">_лпфкаллеррелеасе_</span><span class="sxs-lookup"><span data-stu-id="ae1e2-110">_lpfCallerRelease_</span></span>
  
> <span data-ttu-id="ae1e2-111">возврата Указатель на функцию обратного вызова, основанный на прототипе [каллеррелеасе](callerrelease.md) , который вызывает MAPI при освобождении представления.</span><span class="sxs-lookup"><span data-stu-id="ae1e2-111">[in] A pointer to a callback function based on the [CALLERRELEASE](callerrelease.md) prototype that MAPI calls when it releases the view.</span></span> <span data-ttu-id="ae1e2-112">Если в параметре _лпфкаллеррелеасе_ передается значение null, функция не вызывается в выпуске представления.</span><span class="sxs-lookup"><span data-stu-id="ae1e2-112">If NULL is passed in the  _lpfCallerRelease_ parameter, no function is called on release of the view.</span></span> 
    
 <span data-ttu-id="ae1e2-113">_улкаллердата_</span><span class="sxs-lookup"><span data-stu-id="ae1e2-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="ae1e2-114">возврата Данные, которые должны быть сохранены с новым представлением и переданы в функцию обратного вызова, на которую указывает _лпфкаллеррелеасе_.</span><span class="sxs-lookup"><span data-stu-id="ae1e2-114">[in] The data that must be saved with the new view and passed to the callback function pointed to by  _lpfCallerRelease_.</span></span>
    
 <span data-ttu-id="ae1e2-115">_лппмапитабле_</span><span class="sxs-lookup"><span data-stu-id="ae1e2-115">_lppMAPITable_</span></span>
  
> <span data-ttu-id="ae1e2-116">вышли Указатель на указатель на вновь созданное представление.</span><span class="sxs-lookup"><span data-stu-id="ae1e2-116">[out] A pointer to a pointer to the newly created view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ae1e2-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae1e2-117">Return value</span></span>

<span data-ttu-id="ae1e2-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae1e2-118">S_OK</span></span> 
  
> <span data-ttu-id="ae1e2-119">Представление было успешно создано.</span><span class="sxs-lookup"><span data-stu-id="ae1e2-119">The view was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ae1e2-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="ae1e2-120">Remarks</span></span>

<span data-ttu-id="ae1e2-121">Метод **итабледата:: хржетвиев** создает доступное только для чтения представление данных в таблице, отсортированное в порядке, указанном в параметре _лпссортордерсет_ .</span><span class="sxs-lookup"><span data-stu-id="ae1e2-121">The **ITableData::HrGetView** method creates a read-only view of the data in the table, sorted in the order pointed to by the  _lpSSortOrderSet_ parameter.</span></span> <span data-ttu-id="ae1e2-122">Курсор помещается в начало первой строки представления.</span><span class="sxs-lookup"><span data-stu-id="ae1e2-122">The cursor is placed at the beginning of the first row in the view.</span></span> <span data-ttu-id="ae1e2-123">Возвращается реализация интерфейса **IMAPITable** для доступа к представлению.</span><span class="sxs-lookup"><span data-stu-id="ae1e2-123">An **IMAPITable** interface implementation for accessing the view is returned.</span></span> 
  
<span data-ttu-id="ae1e2-124">Поставщики услуг вызывают **хржетвиев** , когда им нужно предоставить клиентский доступ к таблице.</span><span class="sxs-lookup"><span data-stu-id="ae1e2-124">Service providers call **HrGetView** when they need to give a client access to a table.</span></span> <span data-ttu-id="ae1e2-125">**Хржетвиев** создает представление и возвращает указатель **IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="ae1e2-125">**HrGetView** creates the view and returns the **IMAPITable** pointer.</span></span> <span data-ttu-id="ae1e2-126">Поставщики услуг, в свою очередь, передают указатель клиенту.</span><span class="sxs-lookup"><span data-stu-id="ae1e2-126">Service providers in turn pass the pointer on to the client.</span></span> <span data-ttu-id="ae1e2-127">Когда клиент завершит использование таблицы и вызывает метод [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) , **хржетвиев** вызывает функцию обратного вызова, на которую указывает параметр _лпфкаллеррелеасе_ .</span><span class="sxs-lookup"><span data-stu-id="ae1e2-127">When the client is finished using the table and calls its [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method, **HrGetView** calls the callback function pointed to by the  _lpfCallerRelease_ parameter.</span></span> 
  
<span data-ttu-id="ae1e2-128">Если поставщик услуг должен возвратить клиенту представление с настроенным набором столбцов или ограничением, поставщик может вызвать метод [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) и [IMAPITable:: restrict](imapitable-restrict.md) , прежде чем разрешить клиентский доступ.</span><span class="sxs-lookup"><span data-stu-id="ae1e2-128">If a service provider needs to return to a client a view that has a customized column set or a restriction, the provider can call the view's [IMAPITable::SetColumns](imapitable-setcolumns.md) and [IMAPITable::Restrict](imapitable-restrict.md) methods before allowing the client access.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ae1e2-129">См. также</span><span class="sxs-lookup"><span data-stu-id="ae1e2-129">See also</span></span>



[<span data-ttu-id="ae1e2-130">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="ae1e2-130">CALLERRELEASE</span></span>](callerrelease.md)
  
[<span data-ttu-id="ae1e2-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae1e2-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="ae1e2-132">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="ae1e2-132">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="ae1e2-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae1e2-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

