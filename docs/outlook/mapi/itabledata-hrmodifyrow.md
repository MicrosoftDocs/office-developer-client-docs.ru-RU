---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409001"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вставляет новую строку таблицы, возможно, заменив существующую строку.
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parameters

 _lpSRow_
  
> [in] Указатель на структуру [SRow,](srow.md) описывающую строку, которая должна быть добавлена или заменить существующую строку. Одна из структур значений свойств, на которые указывает член **lpProps** структуры **SRow,** должна содержать столбец индекса, то же значение, которое было задано в параметре _ulPropTagIndexColumn_ в вызове к функции [CreateTable.](createtable.md) 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Строка успешно вставлена или изменена.
    
MAPI_E_INVALID_PARAMETER 
  
> В пройденной строке нет столбца индекса.
    
## <a name="remarks"></a>Примечания

Метод **ITableData::HrModifyRow** вставляет строку, описанную структурой **SRow,** отмеченную параметром _lpSRow._ Если строка, которая имеет то же значение для столбца индекса, что и строка, на которую  _указывает lpSRow,_ уже существует в таблице, будет заменена существующая строка. Если строка не соответствует строке, включенной в структуру **SRow,** **HrModifyRow** добавляет строку в конец таблицы. 
  
Все представления таблицы изменены, чтобы включить строку, на нее указывает _lpSRow._ Однако если представление имеет ограничение, исключаее строки, оно может быть не видно пользователю. 
  
Столбцы в строке, на которые указывает  _lpSRow,_ не должны быть в том же порядке, что и столбцы в таблице. Вызываемая может также включать в качестве столбцов свойства, которые в настоящее время не находятся в таблице. Для существующих представлений **HrModifyRow** делает эти новые столбцы доступными, но не включает их в текущий набор столбцов. Для будущих представлений **HrModifyRow** включает новые столбцы в набор столбцов. 
  
После того, как **HrModifyRow** добавляет строку, уведомления отправляются всем клиентам или поставщикам услуг, которые имеют представление таблицы и которые вызвали метод [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений. 
  
## <a name="see-also"></a>См. также



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

