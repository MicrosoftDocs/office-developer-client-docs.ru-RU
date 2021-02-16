---
title: ITableDataHrDeleteRows
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
  
> [in] Битоваяmas флагов, которая управляет удалением. Можно установить следующий флаг:
    
TAD_ALL_ROWS 
  
> Удаляет все строки из таблицы и всех соответствующих представлений, отправляя одно TABLE_RELOAD уведомления.
    
 _lprowsetToDelete_
  
> [in] Указатель на набор строк, описывая удаляемую строку. Параметр  _lprowsetToDelete_ может иметь TAD_ALL_ROWS NULL, если в параметре  _ulFlags_ установлен флаг TAD_ALL_ROWS. 
    
 _cRowsDeleted_
  
> [out] Количество удаленных строк.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Строки таблицы были успешно удалены.
    
## <a name="remarks"></a>Примечания

Метод **ITableData::HrDeleteRows** находит и удаляет строки таблицы, содержащие столбцы, которые соответствуют свойству, на которое указывает член **lpProps** каждой записи **aRow** в наборе строк. Столбец индекса используется для идентификации каждой строки; Этот столбец должен иметь тот же тег свойства, что и тег свойства, переданный в _параметре ulPropTagIndexColumn_ при вызове [функции CreateTable.](createtable.md) 
  
Количество фактически удаленных строк возвращается в _cRowsDeleted._ Если не удалось найти одну или несколько строк, ошибка не возвращается. 
  
После удаления строк уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и которые вызвали метод [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений. 
  
Удаление строк не уменьшает число столбцов, доступных для существующих представлений таблиц или последующих открытых представлений таблиц, даже если удаленные строки являются последними, имеющими значения для определенного столбца.
  
## <a name="see-also"></a>См. также



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

