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
ms.openlocfilehash: aa2170bf4bedfb441ad4808f774f6f71d5caf85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413271"
---
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отправляет уведомление для строки таблицы.
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _cValues_
  
> [in] Количество значений свойств в [структуре SPropValue,](spropvalue.md) на которые указывает параметр _lpSPropValue._ 
    
 _lpSPropValue_
  
> [in] Указатель на **структуру SPropValue,** которая описывает значения столбцов в целевой строке. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Метод **ITableData::HrNotify** отправляет TABLE_ROW_MODIFIED строку, которая соответствует строке, описанной свойствами, на которые указывает параметр _lpSPropValue._ **HrNotify** отправляет уведомление независимо от того, произошли ли изменения в строке. Все клиенты и поставщики услуг, которые имеют представления таблицы и вызвали [IMAPITable:::Advise,](imapitable-advise.md) чтобы зарегистрироваться для уведомлений о своих представлениях, получают это уведомление. 
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

