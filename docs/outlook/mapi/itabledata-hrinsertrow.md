---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 29fdbf060576ee9309473fddf8740b06229dae9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809588"
---
# <a name="itabledatahrinsertrow"></a>ITableData::HrInsertRow

  
  
**Относится к**: Outlook 
  
Вставляет строку в таблице. 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Параметры

 _uliRow_
  
> [in] Номер последовательного строки, который представляет определенную строку. Новая строка будет помещен после строки, которая указывает номер. Параметр _uliRow_ может содержать номера строк от 0 до n, где n — общее число строк в таблице. Передача n в _uliRow_ добавляет строку в конец таблицы. 
    
 _lpSRow_
  
> [in] Указатель на структуру [SRow](srow.md) , описывающую строку, которую нужно вставить. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Успешно добавления строки.
    
MAPI_E_INVALID_PARAMETER 
  
> Строка, которая имеет такое же значение для его индекс столбца как строку для вставки уже существует в таблице.
    
## <a name="remarks"></a>Замечания

Метод **ITableData::HrInsertRow** вставляет строку в таблицу в определенное место. Новая строка будет вставлена после строку, в которой находится в положение, указанного с помощью параметра _uliRow_ . 
  
Если число строк в таблице _uliRow_ , новая строка добавляется в конец таблицы. 
  
Свойство действует как индекс столбца для таблицы должны быть включены в член **lpProps** структуры [SRow](srow.md) указывает параметр _lpSRow_ . Это свойство индекса, обычно **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) используется для уникальной идентификации строки для задач, будущее обслуживание системы.
  
Свойство столбцы в структуре **SRow** нет необходимости находиться в том же порядке, как в столбцы свойств в таблице. 
  
После вставки строки уведомления отправляются для всех клиентов или поставщиков услуг, у которых представление таблицы и, вызова метода [IMAPITable::Advise](imapitable-advise.md) таблицы для регистрации уведомлений. Если вставленной строки не включен в представление, из-за ограничения отправляется без уведомления. 
  
## <a name="see-also"></a>См. также



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

