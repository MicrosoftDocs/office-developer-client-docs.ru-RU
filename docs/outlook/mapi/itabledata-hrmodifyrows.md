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
ms.openlocfilehash: 06356d60b43d7e5be61d944c07001570bdd5c678
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571110"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Вставка нескольких строк таблицы, возможно замена существующих строк.
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpSRowSet_
  
> [in] Указатель на структуру [SRowSet](srowset.md) , которая содержит набор строк, добавлена, замена существующих строк, если это необходимо. Один из структур значение свойства, по **lpProps** членом каждого [SRow](srow.md) структуру в строку, на который указывает должен содержать столбце индекса такое же значение, которое было указано в параметре _ulPropTagIndexColumn_ в вызове [ CreateTable](createtable.md) функции. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Строки были успешно добавлены или изменены.
    
MAPI_E_INVALID_PARAMETER 
  
> Один или несколько строк, переданное нет столбца индекса. Если этой ошибки строки не изменяются.
    
## <a name="remarks"></a>Замечания

Метод **ITableData::HrModifyRows** вставляет строки, описанные в структуре [SRowSet](srowset.md) указывает параметр _lpSRowSet_ . Если значение столбца индекс строки в наборе строк совпадает со значением для существующей строки в таблице, будет заменен существующей строки. Если нет строки, которая соответствует того, что включено в структуре **SRowSet** , **HrModifyRows** добавляет строку в конец таблицы. 
  
Все представления таблицы изменяются, чтобы включить строки, на который указывает _lpSRowSet_. Тем не менее если представление имеет ограничение на месте, которое не содержит строку, он может оказаться видимым для пользователя. 
  
Столбцы в строках, на который указывает _lpSRowSet_ нет необходимости находиться в том же порядке в виде столбцов в таблице. Звонящий может также содержать как свойства столбцов, которые в настоящее время не в таблице. Для существующего представления **HrModifyRows** делает доступными этих новых столбцов, но не включать их в текущий набор столбцов. Для будущего представлений **HrModifyRows** включает в себя новые столбцы в наборе столбцов. 
  
После добавления строки **HrModifyRows** уведомления отправляются для всех клиентов или поставщиков услуг, у которых представление таблицы и, вызова метода [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений. MAPI отправляет уведомления TABLE_ROW_ADDED или TABLE_ROW_MODIFIED для каждой строки до восьми строк. Если влияет на более восьми строк путем вызова **HrModifyRows** , MAPI отправляет уведомление об одном TABLE_CHANGED, вместо этого. 
  
## <a name="see-also"></a>См. также



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

