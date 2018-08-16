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
ms.openlocfilehash: a1388545597cf0000f270bf693c93f9349fb6426
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809616"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**Относится к**: Outlook 
  
Добавление новой строки в таблице, возможно заменить существующую строку.
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Параметры

 _lpSRow_
  
> [in] Указатель на структуру [SRow](srow.md) , описывающую строку добавить или заменить существующую строку. Один структур значение свойства, на который указывает член **lpProps** структуры **SRow** должен содержать столбце индекса такое же значение, которое было указано в параметре _ulPropTagIndexColumn_ в вызове [CreateTable ](createtable.md)функции. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Строки были успешно добавлены или изменены.
    
MAPI_E_INVALID_PARAMETER 
  
> Строка переданное не имеет столбец индекса.
    
## <a name="remarks"></a>Замечания

Метод **ITableData::HrModifyRow** вставляет строку, описанного в структуре **SRow** указывает параметр _lpSRow_ . Если строку, в которой имеет такое же значение для его индекс столбца как строку, указывающий _lpSRow_ уже существует в таблице, будет заменен существующей строки. Если нет строки, которая соответствует того, что включено в структуре **SRow** , **HrModifyRow** добавляет строку в конец таблицы. 
  
Все представления таблицы изменяются, чтобы включить строку, на который указывает _lpSRow_. Тем не менее если представление имеет ограничение на месте, которое не содержит строку, он может оказаться видимым для пользователя. 
  
Столбцы в строке, на который указывает _lpSRow_ нет необходимости находиться в том же порядке в виде столбцов в таблице. Звонящий может также содержать как свойства столбцов, которые в настоящее время не в таблице. Для существующего представления **HrModifyRow** делает доступными этих новых столбцов, но не включать их в текущий набор столбцов. Для будущего представлений **HrModifyRow** включает в себя новые столбцы в наборе столбцов. 
  
После **HrModifyRow** добавляет строку, уведомления отправляются для всех клиентов или поставщиков услуг, у которых представление таблицы и, вызова метода [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений. 
  
## <a name="see-also"></a>См. также



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)
