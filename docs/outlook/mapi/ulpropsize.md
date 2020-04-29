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
ms.openlocfilehash: cc1547ad7d881b707825630f96987d4c40ad4863
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416904"
---
# <a name="ulpropsize"></a>UlPropSize

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает размер одного значения свойства. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
ULONG UlPropSize(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Параметры

 _лпспропвалуе_
  
> возврата Указатель на структуру [спропвалуе](spropvalue.md) , определяющую свойство, которое необходимо измерить. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_CALL_FAILED 
  
> Не удалось завершить операцию из — из — из — из — из — из — из неизвестного источника.
    
## <a name="remarks"></a>Примечания

Функция **улпропсизе** возвращает размер (в байтах) значения свойства для указанного свойства. Он не зависит от размера оставшейся части структуры **спропвалуе** . 
  

