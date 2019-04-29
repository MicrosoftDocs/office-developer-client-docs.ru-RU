---
title: Итабледатахрделетеровс
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fdd6f40b4d7aa7f65bf1a46d3d9a4f18472b19f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416456"
---
# <a name="itabledatahrdeleterows"></a>ITableData::HrDeleteRows

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Удаляет несколько строк таблицы.
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, которые управляют удалением. Можно задать следующий флаг:
    
ТАД_АЛЛ_РОВС 
  
> Удаляет все строки из таблицы и всех соответствующих представлений, отправляя одно уведомление ТАБЛЕ_РЕЛОАД.
    
 _Лпровсеттоделете_
  
> возврата Указатель на набор строк, который описывает удаляемые строки. Параметр _лпровсеттоделете_ может иметь значение null, если установлен флаг тад_алл_ровс в параметре _ulFlags_ . 
    
 _Кровсделетед_
  
> вышли Количество удаленных строк.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Строки таблицы были успешно удалены.
    
## <a name="remarks"></a>Примечания

Метод **итабледата:: хрделетеровс** ищет и удаляет строки таблицы, которые содержат столбцы, которые совпадают со свойством, на которое указывает элемент **лппропс** для каждой записи **аров** в наборе строк. Столбец индекса используется для идентификации каждой строки; Этот столбец должен иметь тот же тег Property, что и тег свойства, переданный в параметре _улпроптагиндексколумн_ при вызове функции [креатетабле](createtable.md) . 
  
Количество фактически удаленных строк возвращается в _кровсделетед_. Сообщение об ошибке не возвращается, если не удалось найти одну или несколько строк. 
  
После удаления строк уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и вызывают метод [IMAPITable:: Advise](imapitable-advise.md) для регистрации уведомлений. 
  
Удаление строк не приводит к уменьшению числа столбцов, доступных для существующих представлений таблицы или представления таблицы в открытых окнах, даже если удаленные строки являются последними значениями для определенного столбца.
  
## <a name="see-also"></a>См. также



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

