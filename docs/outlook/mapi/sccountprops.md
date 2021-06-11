---
title: ScCountProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountProps
api_type:
- COM
ms.assetid: 76e4cc52-e1a0-4e0b-a2a6-a17644f6b2e7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 49634bda487143ddd8d8806b94f6c451ccf57b75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404976"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет размер в bytes массива значений свойств и проверяет память, связанную с массивом. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameters

 _cprop_
  
> [in] Количество свойств в массиве, указанных параметром _rgprop._ 
    
 _rgprop_
  
> [in] Указатель на диапазон в массиве [структур SPropValue,](spropvalue.md) определяя свойства, размер которых должен быть определен. Этот диапазон не обязательно начинается в начале массива. 
    
 _pcb_
  
> [вышел] Необязательный указатель на размер в bytes массива свойств.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_INVALID_PARAMETER 
  
> По крайней мере одно свойство в массиве значений свойств имеет идентификатор PROP_ID_NULL или PROP_ID_INVALID или массив свойств содержит многоценное свойство без значений свойств.
    
## <a name="remarks"></a>Примечания

Если NULL передается в  _параметре PCB,_ функция **ScCountProps** проверяет массив уведомлений, но подсчет не делается. Если значение non-null передается в _pcb,_ функция **ScCountNotifications** определяет размер массива и сохраняет причину _pcb._ Параметр  _PCB_ должен быть достаточно большим, чтобы содержать весь массив. 
  
При подсчете **scCountProps** проверяет память, связанную с массивом. **ScCountProps** работает только с свойствами, сведения о которых имеются в MAPI. 
  
## <a name="see-also"></a>См. также



[PropCopyMore](propcopymore.md)

