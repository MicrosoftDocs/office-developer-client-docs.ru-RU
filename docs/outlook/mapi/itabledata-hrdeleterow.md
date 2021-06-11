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
ms.openlocfilehash: b187cccc4505256b7ab4d580c30eeb2e15ebf574
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421678"
---
# <a name="itabledatahrdeleterow"></a><span data-ttu-id="f7736-103">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="f7736-103">ITableData::HrDeleteRow</span></span>

  
  
<span data-ttu-id="f7736-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7736-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7736-105">Удаляет строку таблицы.</span><span class="sxs-lookup"><span data-stu-id="f7736-105">Deletes a table row.</span></span>
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="f7736-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f7736-106">Parameters</span></span>

 <span data-ttu-id="f7736-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="f7736-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="f7736-108">[in] Указатель на структуру значения свойства, описываемую столбец индекса для строки, которая должна быть удалена.</span><span class="sxs-lookup"><span data-stu-id="f7736-108">[in] A pointer to a property value structure that describes the index column for the row to be deleted.</span></span> <span data-ttu-id="f7736-109">Член структуры значения свойства **ulPropTag** должен содержать тот же тег свойства, что и _параметр ulPropTagIndexColumn_ от вызова до [функции CreateTable.](createtable.md)</span><span class="sxs-lookup"><span data-stu-id="f7736-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f7736-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7736-110">Return value</span></span>

<span data-ttu-id="f7736-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="f7736-111">S_OK</span></span> 
  
> <span data-ttu-id="f7736-112">Строка успешно удалена.</span><span class="sxs-lookup"><span data-stu-id="f7736-112">The row was successfully deleted.</span></span>
    
<span data-ttu-id="f7736-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f7736-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="f7736-114">Свойство, на который указывает параметр  _lpSPropValue,_ не определяет строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="f7736-114">The property pointed to by the  _lpSPropValue_ parameter does not identify a row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f7736-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="f7736-115">Remarks</span></span>

<span data-ttu-id="f7736-116">Метод **ITableData::HrDeleteRow** удаляет строку таблицы, которая содержит столбец, который соответствует свойству, на которое указывает параметр _lpSPropValue._</span><span class="sxs-lookup"><span data-stu-id="f7736-116">The **ITableData::HrDeleteRow** method removes the table row that contains the column that matches the property pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="f7736-117">Данные для строки удаляются, а строка удаляется из всех открытых представлений.</span><span class="sxs-lookup"><span data-stu-id="f7736-117">The data for the row is deleted and the row is removed from all open views.</span></span> 
  
<span data-ttu-id="f7736-118">После удаления строки уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и которые вызвали метод [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="f7736-118">After the row is deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="f7736-119">Удаление строки не уменьшает набор столбцов, доступный для существующих представлений или впоследствии открытых представлений, даже если удаленная строка является последней строкой, имеющей значение для определенного столбца.</span><span class="sxs-lookup"><span data-stu-id="f7736-119">Deleting a row does not reduce the column set that is available to existing views or subsequently opened views, even if the deleted row is the last row that has a value for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f7736-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f7736-120">See also</span></span>



[<span data-ttu-id="f7736-121">CreateTable</span><span class="sxs-lookup"><span data-stu-id="f7736-121">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="f7736-122">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="f7736-122">ITableData::HrDeleteRows</span></span>](itabledata-hrdeleterows.md)
  
[<span data-ttu-id="f7736-123">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="f7736-123">ITableData::HrModifyRow</span></span>](itabledata-hrmodifyrow.md)
  
[<span data-ttu-id="f7736-124">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f7736-124">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="f7736-125">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f7736-125">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="f7736-126">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f7736-126">ITableData : IUnknown</span></span>](itabledataiunknown.md)

