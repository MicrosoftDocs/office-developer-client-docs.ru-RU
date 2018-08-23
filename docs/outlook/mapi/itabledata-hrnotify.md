---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 20831901567f177ada70a6cea94db0537786db94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571439"
---
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Отправляет уведомления для строки в таблице.
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _cValues_
  
> [in] Число значений свойств в структуре [SPropValue](spropvalue.md) указывает параметр _lpSPropValue_ . 
    
 _lpSPropValue_
  
> [in] Указатель на структуру **SPropValue** , описаны значения столбцов в строки целевое значение. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Метод **ITableData::HrNotify** отправляет уведомление TABLE_ROW_MODIFIED для строки, которая соответствует строке, описываемого свойства, на который указывает параметр _lpSPropValue_ . **HrNotify** отправляет уведомление, независимо от того, является ли изменений в строку. Все клиенты и поставщиков услуг, которые имеют представления таблицы и вызова [IMAPITable::Advise](imapitable-advise.md) для регистрации уведомлений на их представления получать уведомления. 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

