---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d0074dd006fda6d44252011d0b979169e0c3d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405361"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вставляет несколько строк таблицы, возможно, заменяя существующие строки.
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpSRowSet_
  
> [in] Указатель на структуру [SRowSet,](srowset.md) содержающую набор строк, которые необходимо добавить, заменив при необходимости существующие строки. Одна из структур значений свойств, на которую указывает член **lpProps** каждой структуры [SRow](srow.md) в наборе строк, должна содержать столбец индекса, то же значение, которое было задано в параметре _ulPropTagIndexColumn_ в вызове к функции [CreateTable.](createtable.md) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Строки успешно вставлены или изменены.
    
MAPI_E_INVALID_PARAMETER 
  
> Одна или несколько из переданных строк не имеют столбца индекса. Если эта ошибка возвращается, строки не будут изменены.
    
## <a name="remarks"></a>Примечания

Метод **ITableData::HrModifyRows** вставляет строки, описанные структурой [SRowSet,](srowset.md) на которые указывает параметр _lpSRowSet._ Если значение столбца индекса строки в наборе строк соответствует значению существующей строки в таблице, существующая строка заменяется. Если строка не соответствует строке, включенной в структуру **SRowSet,** **HrModifyRows** добавляет строку в конец таблицы. 
  
Все представления таблицы изменены, чтобы включить строки, на которые указывает _lpSRowSet._ Однако если представление имеет ограничение, исключаее строки, оно может не быть видимым пользователю. 
  
Столбцы в строках, на которые указывает  _lpSRowSet,_ не должны быть в том же порядке, что и столбцы в таблице. Вызываемая может также включать в качестве столбцов свойства, которые в настоящее время не находятся в таблице. Для существующих представлений **HrModifyRows** делает эти новые столбцы доступными, но не включает их в текущий набор столбцов. Для будущих представлений **HrModifyRows** включает новые столбцы в наборе столбцов. 
  
После того как **hrModifyRows** добавил строки, уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и которые вызвали метод [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений. MAPI отправляет TABLE_ROW_ADDED или TABLE_ROW_MODIFIED уведомления для каждой строки до восьми строк. Если вызов **HrModifyRows** затрагивает более восьми строк, MAPI отправляет вместо этого TABLE_CHANGED одно уведомление. 
  
## <a name="see-also"></a>См. также



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

