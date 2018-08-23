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
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Удаляет строку в таблице.
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Параметры

 _lpSPropValue_
  
> [in] Указатель на структуру значение свойства, с описанием столбца индекса для строки для удаления. Член **ulPropTag** структуры значение свойства должны содержать один и тот же свойство тег параметра- _ulPropTagIndexColumn_ вызов функции [CreateTable](createtable.md) . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Строка успешно удалена.
    
MAPI_E_NOT_FOUND 
  
> Свойство указывает параметр _lpSPropValue_ не определяет строку в таблице. 
    
## <a name="remarks"></a>Замечания

Метод **ITableData::HrDeleteRow** удаляет строку в таблице, которая содержит столбец, который сопоставляет свойство указывает параметр _lpSPropValue_ . Данные для строки удаляются и строка удаляется из всех открытых представлений. 
  
После удаления строки уведомления отправляются для всех клиентов или поставщиков услуг, у которых представление таблицы и, вызова метода [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений. 
  
Удаление строки не уменьшает набор столбцов, доступных для существующего представления или впоследствии открытых представлений, даже если к удаленной строки последней строки, который имеет значение для определенного столбца.
  
## <a name="see-also"></a>См. также



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

