---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 989c6872e78ef78e5e0b18149a186d4f920ca603
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563466"
---
# <a name="itabledatahrdeleterow"></a><span data-ttu-id="1005d-103">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="1005d-103">ITableData::HrDeleteRow</span></span>

  
  
<span data-ttu-id="1005d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1005d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1005d-105">Удаляет строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="1005d-105">Deletes a table row.</span></span>
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="1005d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1005d-106">Parameters</span></span>

 <span data-ttu-id="1005d-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="1005d-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="1005d-108">[in] Указатель на структуру значение свойства, с описанием столбца индекса для строки для удаления.</span><span class="sxs-lookup"><span data-stu-id="1005d-108">[in] A pointer to a property value structure that describes the index column for the row to be deleted.</span></span> <span data-ttu-id="1005d-109">Член **ulPropTag** структуры значение свойства должны содержать один и тот же свойство тег параметра- _ulPropTagIndexColumn_ вызов функции [CreateTable](createtable.md) .</span><span class="sxs-lookup"><span data-stu-id="1005d-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1005d-110">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1005d-110">Return value</span></span>

<span data-ttu-id="1005d-111">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="1005d-111">S_OK</span></span> 
  
> <span data-ttu-id="1005d-112">Строка успешно удалена.</span><span class="sxs-lookup"><span data-stu-id="1005d-112">The row was successfully deleted.</span></span>
    
<span data-ttu-id="1005d-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="1005d-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="1005d-114">Свойство указывает параметр _lpSPropValue_ не определяет строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="1005d-114">The property pointed to by the  _lpSPropValue_ parameter does not identify a row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1005d-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="1005d-115">Remarks</span></span>

<span data-ttu-id="1005d-116">Метод **ITableData::HrDeleteRow** удаляет строку в таблице, которая содержит столбец, который сопоставляет свойство указывает параметр _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="1005d-116">The **ITableData::HrDeleteRow** method removes the table row that contains the column that matches the property pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="1005d-117">Данные для строки удаляются и строка удаляется из всех открытых представлений.</span><span class="sxs-lookup"><span data-stu-id="1005d-117">The data for the row is deleted and the row is removed from all open views.</span></span> 
  
<span data-ttu-id="1005d-118">После удаления строки уведомления отправляются для всех клиентов или поставщиков услуг, у которых представление таблицы и, вызова метода [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="1005d-118">After the row is deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="1005d-119">Удаление строки не уменьшает набор столбцов, доступных для существующего представления или впоследствии открытых представлений, даже если к удаленной строки последней строки, который имеет значение для определенного столбца.</span><span class="sxs-lookup"><span data-stu-id="1005d-119">Deleting a row does not reduce the column set that is available to existing views or subsequently opened views, even if the deleted row is the last row that has a value for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1005d-120">См. также</span><span class="sxs-lookup"><span data-stu-id="1005d-120">See also</span></span>



[<span data-ttu-id="1005d-121">CreateTable</span><span class="sxs-lookup"><span data-stu-id="1005d-121">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="1005d-122">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="1005d-122">ITableData::HrDeleteRows</span></span>](itabledata-hrdeleterows.md)
  
[<span data-ttu-id="1005d-123">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="1005d-123">ITableData::HrModifyRow</span></span>](itabledata-hrmodifyrow.md)
  
[<span data-ttu-id="1005d-124">SPropValue</span><span class="sxs-lookup"><span data-stu-id="1005d-124">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="1005d-125">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1005d-125">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="1005d-126">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1005d-126">ITableData : IUnknown</span></span>](itabledataiunknown.md)

