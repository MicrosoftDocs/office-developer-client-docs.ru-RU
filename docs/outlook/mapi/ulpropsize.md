---
title: UlPropSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlPropSize
api_type:
- COM
ms.assetid: 240f1144-0805-4cd1-9e7d-f2a550a2f160
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2bfe2841592987c530f6323db94834c1dcb64b2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576640"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает размер значения одного свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Параметры

 _lpSPropValue_
  
> [in] Указатель на структуру [SPropValue](spropvalue.md) определение свойства, которое должно быть измеряется. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_CALL_FAILED 
  
> Ошибка непредвиденные или неизвестный происхождения запрещено выполнение операции.
    
## <a name="remarks"></a>Замечания

Функция **UlPropSize** возвращает размер, в байтах, значение свойства для указанного свойства. Она игнорирует размер в оставшейся части структуры **SPropValue** . 
  

