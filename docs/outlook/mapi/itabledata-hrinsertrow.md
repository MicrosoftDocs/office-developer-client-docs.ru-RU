---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 29fdbf060576ee9309473fddf8740b06229dae9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809588"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="785d9-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="785d9-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="785d9-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="785d9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="785d9-105">Вставляет строку в таблице.</span><span class="sxs-lookup"><span data-stu-id="785d9-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="785d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="785d9-106">Parameters</span></span>

 <span data-ttu-id="785d9-107">_uliRow_</span><span class="sxs-lookup"><span data-stu-id="785d9-107">_uliRow_</span></span>
  
> <span data-ttu-id="785d9-108">[in] Номер последовательного строки, который представляет определенную строку.</span><span class="sxs-lookup"><span data-stu-id="785d9-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="785d9-109">Новая строка будет помещен после строки, которая указывает номер.</span><span class="sxs-lookup"><span data-stu-id="785d9-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="785d9-110">Параметр _uliRow_ может содержать номера строк от 0 до n, где n — общее число строк в таблице.</span><span class="sxs-lookup"><span data-stu-id="785d9-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="785d9-111">Передача n в _uliRow_ добавляет строку в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="785d9-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="785d9-112">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="785d9-112">_lpSRow_</span></span>
  
> <span data-ttu-id="785d9-113">[in] Указатель на структуру [SRow](srow.md) , описывающую строку, которую нужно вставить.</span><span class="sxs-lookup"><span data-stu-id="785d9-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="785d9-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4">Return value</span></span>

<span data-ttu-id="785d9-115">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="785d9-115">S_OK</span></span> 
  
> <span data-ttu-id="785d9-116">Успешно добавления строки.</span><span class="sxs-lookup"><span data-stu-id="785d9-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="785d9-117">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="785d9-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="785d9-118">Строка, которая имеет такое же значение для его индекс столбца как строку для вставки уже существует в таблице.</span><span class="sxs-lookup"><span data-stu-id="785d9-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="785d9-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="785d9-119">Remarks</span></span>

<span data-ttu-id="785d9-120">Метод **ITableData::HrInsertRow** вставляет строку в таблицу в определенное место.</span><span class="sxs-lookup"><span data-stu-id="785d9-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="785d9-121">Новая строка будет вставлена после строку, в которой находится в положение, указанного с помощью параметра _uliRow_ .</span><span class="sxs-lookup"><span data-stu-id="785d9-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="785d9-122">Если число строк в таблице _uliRow_ , новая строка добавляется в конец таблицы.</span><span class="sxs-lookup"><span data-stu-id="785d9-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="785d9-123">Свойство действует как индекс столбца для таблицы должны быть включены в член **lpProps** структуры [SRow](srow.md) указывает параметр _lpSRow_ .</span><span class="sxs-lookup"><span data-stu-id="785d9-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="785d9-124">Это свойство индекса, обычно **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) используется для уникальной идентификации строки для задач, будущее обслуживание системы.</span><span class="sxs-lookup"><span data-stu-id="785d9-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="785d9-125">Свойство столбцы в структуре **SRow** нет необходимости находиться в том же порядке, как в столбцы свойств в таблице.</span><span class="sxs-lookup"><span data-stu-id="785d9-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="785d9-126">После вставки строки уведомления отправляются для всех клиентов или поставщиков услуг, у которых представление таблицы и, вызова метода [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="785d9-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="785d9-127">Если вставленной строки не включен в представление, из-за ограничения отправляется без уведомления.</span><span class="sxs-lookup"><span data-stu-id="785d9-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="785d9-128">См. также</span><span class="sxs-lookup"><span data-stu-id="785d9-128">See also</span></span>



[<span data-ttu-id="785d9-129">SRow</span><span class="sxs-lookup"><span data-stu-id="785d9-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="785d9-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="785d9-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="785d9-131">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="785d9-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

