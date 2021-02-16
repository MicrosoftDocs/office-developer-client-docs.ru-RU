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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет размер массива значений свойств (в bytes) и проверяет память, связанную с массивом. 
  
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

## <a name="parameters"></a>Параметры

 _cprop_
  
> [in] Количество свойств в массиве, указанных _параметром rgprop._ 
    
 _rgprop_
  
> [in] Указатель на диапазон в массиве [структур SPropValue,](spropvalue.md) который определяет свойства, размер которых необходимо определить. Этот диапазон необязательно начинается с начала массива. 
    
 _pcb_
  
> [out] Необязательный указатель на размер массива свойств (в bytes).
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_INVALID_PARAMETER 
  
> По крайней мере одно свойство в массиве значений свойств имеет идентификатор PROP_ID_NULL или PROP_ID_INVALID или массив свойств содержит многоценное свойство без значений свойств.
    
## <a name="remarks"></a>Примечания

Если в параметре  _PCB_ передается NULL, функция **ScCountProps** проверяет массив уведомлений, но подсчет не делается. Если в _pcb_ передается ненулевое значение, функция **ScCountNotifications** определяет размер массива и сохраняет ПХБ _причины._ Параметр  _pcb_ должен быть достаточно большим, чтобы содержать весь массив. 
  
При подсчете **ScCountProps** проверяет память, связанную с массивом. **ScCountProps** работает только со свойствами, сведения о которых есть в MAPI. 
  
## <a name="see-also"></a>См. также



[PropCopyMore](propcopymore.md)

