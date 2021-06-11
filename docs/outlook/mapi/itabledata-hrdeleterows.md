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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет несколько строк таблицы.
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмашка флагов, которые контролируют удаление. Можно установить следующий флаг:
    
TAD_ALL_ROWS 
  
> Удаляет все строки из таблицы и все соответствующие представления, отправляя TABLE_RELOAD уведомления.
    
 _lprowsetToDelete_
  
> [in] Указатель на набор строк, который описывает удаляемые строки. Параметр _lprowsetToDelete_ может быть NULL, если флаг TAD_ALL_ROWS в _параметре ulFlags._ 
    
 _cRowsDeleted_
  
> [вышел] Количество удаленных строк.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Строки таблиц были успешно удалены.
    
## <a name="remarks"></a>Примечания

Метод **ITableData::HrDeleteRows** находит и удаляет строки таблиц, содержащие столбцы, которые соответствуют свойству, на которое указывает участник **lpProps** каждой записи **aRow** в наборе строк. Столбец индекса используется для определения каждой строки; Этот столбец должен иметь тот же тег свойств, что и тег свойства, переданный в _параметре ulPropTagIndexColumn_ в вызове к функции [CreateTable.](createtable.md) 
  
Количество строк, которые были фактически удалены, возвращается _в cRowsDeleted._ Ошибка не возвращается, если не удалось найти одну или несколько строк. 
  
После удаления строк уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и которые вызвали метод [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений. 
  
Удаление строк не уменьшает количество столбцов, доступных для существующих представлений таблиц или впоследствии открытых представлений таблиц, даже если удаленные строки являются последними, имеющими значения для определенного столбца.
  
## <a name="see-also"></a>См. также



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

