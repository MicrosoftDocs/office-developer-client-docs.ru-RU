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
ms.openlocfilehash: 97dad50fed4179526e46381c4d9ea9d12d568377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812223"
---
# <a name="sccountprops"></a>ScCountProps

  
  
**Относится к**: Outlook 
  
Определяет размер в байтах, массива значение свойства и проверяет память, связанную с массивом. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE ScCountProps(
  int cprop,
  LPSPropValue rgprop,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Параметры

 _cprop_
  
> [in] Число свойств в массива, указанного в параметре _rgprop_ . 
    
 _rgprop_
  
> [in] Указатель для диапазона ячеек в массив структур [SPropValue](spropvalue.md) , который определяет свойства, размер которого будет определено. Этот диапазон не обязательно запускается в начале массива. 
    
 _печатной_
  
> [out] Необязательный указатель на размер, в байтах, свойство массива.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_INVALID_PARAMETER 
  
> По крайней мере одно свойство в массиве значение свойства имеет идентификатор PROP_ID_NULL или PROP_ID_INVALID или массива свойства содержит многозначного свойства нет значения свойства.
    
## <a name="remarks"></a>Замечания

Если в параметре _печатной_ передано значение NULL, функция **ScCountProps** проверяет массива уведомления о, но инвентаризации не выполняется. Если ненулевое значение передается в _печатной_, функция **ScCountNotifications** определяет размер массива и сохраняет несколько _печатной_. Параметр _печатной_ должен быть достаточно большим для размещения всего массива. 
  
Как подсчет, **ScCountProps** проверяет память, связанную с массивом. **ScCountProps** работает только со свойствами, о том, какие заполнению MAPI. 
  
## <a name="see-also"></a>См. также



[PropCopyMore](propcopymore.md)

