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
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет строку таблицы.
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parameters

 _lpSPropValue_
  
> [in] Указатель на структуру значения свойства, описываемую столбец индекса для строки, которая должна быть удалена. Член структуры значения свойства **ulPropTag** должен содержать тот же тег свойства, что и _параметр ulPropTagIndexColumn_ от вызова до [функции CreateTable.](createtable.md) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Строка успешно удалена.
    
MAPI_E_NOT_FOUND 
  
> Свойство, на который указывает параметр  _lpSPropValue,_ не определяет строку в таблице. 
    
## <a name="remarks"></a>Примечания

Метод **ITableData::HrDeleteRow** удаляет строку таблицы, которая содержит столбец, который соответствует свойству, на которое указывает параметр _lpSPropValue._ Данные для строки удаляются, а строка удаляется из всех открытых представлений. 
  
После удаления строки уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и которые вызвали метод [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений. 
  
Удаление строки не уменьшает набор столбцов, доступный для существующих представлений или впоследствии открытых представлений, даже если удаленная строка является последней строкой, имеющей значение для определенного столбца.
  
## <a name="see-also"></a>См. также



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

