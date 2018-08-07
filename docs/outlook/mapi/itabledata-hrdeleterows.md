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
ms.openlocfilehash: 00662d7a5bf1c2addc5c4e0b39d657abd7073753
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809589"
---
# <a name="itabledatahrdeleterows"></a>ITableData::HrDeleteRows

  
  
**Относится к**: Outlook 
  
Удаление нескольких строк таблицы.
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который управляет удаления. Можно задать следующий флаг:
    
TAD_ALL_ROWS 
  
> Удаляет все строки из таблицы и все соответствующие представления, отправки одного TABLE_RELOAD уведомления.
    
 _lprowsetToDelete_
  
> [in] Указатель на набор строк, с описанием удаляемых строк. Параметр _lprowsetToDelete_ может быть NULL, если флаг TAD_ALL_ROWS установлен в параметре _ulFlags_ . 
    
 _cRowsDeleted_
  
> [out] Число удаленных строк.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Строки таблицы были успешно удалены.
    
## <a name="remarks"></a>Замечания

Метод **ITableData::HrDeleteRows** обнаруживает и удаляет строки в таблице, содержащие столбцы, которые соответствуют по **lpProps** членом каждой записи **aRow** в строке, на который указывает свойство. Столбец индекса используется для идентификации каждой строки; Этот столбец должен иметь один и тот же тег свойство как свойство tag, переданной в параметре _ulPropTagIndexColumn_ в вызове функции [CreateTable](createtable.md) . 
  
Количество строк, которые фактически были удалены, возвращается в _cRowsDeleted_. Сообщение об ошибке не возвращается, если не удается найти один или несколько строк. 
  
После удаления строки уведомления отправляются для всех клиентов или поставщиков услуг, у которых представление таблицы и, вызова метода [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений. 
  
Удаление строк не уменьшает столбцов, доступных для существующего представления таблицы или впоследствии открывается представления таблицы, даже если удаленных строк, последний, имеют значения для определенного столбца.
  
## <a name="see-also"></a>См. также



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

