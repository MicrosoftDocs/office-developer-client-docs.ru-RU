---
title: Итабледатахрделетеров
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278862"
---
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет строку таблицы.
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Параметры

 _Лпспропвалуе_
  
> возврата Указатель на структуру значения свойства, которая описывает столбец индекса для удаляемой строки. Элемент **улпроптаг** структуры значения свойства должен содержать тот же тег свойства, что и параметр _улпроптагиндексколумн_ , из вызова функции [креатетабле](createtable.md) . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Строка была успешно удалена.
    
МАПИ_Е_НОТ_ФАУНД 
  
> Свойство, на которое указывает параметр _лпспропвалуе_ , не определяет строку в таблице. 
    
## <a name="remarks"></a>Замечания

Метод **итабледата:: хрделетеров** удаляет строку таблицы, содержащую столбец, который соответствует свойству, на которую указывает параметр _лпспропвалуе_ . Данные для строки удаляются, а строка удаляется из всех открытых представлений. 
  
После удаления строки уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и вызывают метод [IMAPITable:: Advise](imapitable-advise.md) для регистрации уведомлений. 
  
Удаление строки не уменьшает набор столбцов, доступный для существующих представлений или последовательного представления, даже если удаленная строка является последней строкой, содержащей значение для определенного столбца.
  
## <a name="see-also"></a>См. также



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

