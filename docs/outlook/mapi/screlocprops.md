---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421090"
---
# <a name="screlocprops"></a>ScRelocProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Корректирует указатели в [массиве SPropValue](spropvalue.md) после копирования массива и его данных в новом расположении. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameters

 _cprop_
  
> [in] Количество свойств в массиве, на который указывает параметр _rgprop._ 
    
 _rgprop_
  
> [in] Указатель на массив [структур SPropValue,](spropvalue.md) для которых необходимо корректировать указатели. 
    
 _pvBaseOld_
  
> [in] Указатель на исходный базовый адрес массива, на который указывает параметр _rgprop._ 
    
 _pvBaseNew_
  
> [in] Указатель на новый базовый адрес массива, на который указывает параметр _rgprop._ 
    
 _pcb_
  
> [in, out] Необязательный указатель на размер в bytes массива, указанный _параметром pvBaseNew._ Если не NULL, параметр _PCB_ задан для количества bytes, хранимого в _параметре pvD._ 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Указатели были успешно скорректированы.
    
MAPI_E_INVALID_PARAMETER
  
> Один или оба параметра были недействительны, или был встречен неизвестный тип свойства.
    
## <a name="remarks"></a>Примечания

Функция **ScRelocProps** работает на предположении, что массив значений свойств, для которого корректируются указатели, первоначально был выделен в одном вызове, аналогичном вызову функции **ScCopyProps.** Если клиентские приложения или поставщик услуг работают со значением свойства, которое построено из разрощенных блоков памяти, для копирования свойств следует использовать [ScCopyProps.](sccopyprops.md) 
  
 **ScRelocProps** используется для поддержания действительности указателей в [массиве SPropValue.](spropvalue.md) Чтобы сохранить достоверность указателей при записи такого массива на диск и его прочтения, выполните следующие операции: 
  
1. Перед записью массива и данных на диск вызываем **scRelocProps** на массиве с параметром  _pvBaseNew,_ указыв, например, на некоторое стандартное значение ноль. 
    
2. После прочтения массива и данных с диска вызываем **ScRelocProps** на массиве с параметром  _pvBaseOld,_ равным стандартному значению, используемом в шаге 1. Массив и данные необходимо считыть в буфер, созданный с одним выделением. 
    
3. Параметр  _pcb_ для **ScRelocProps** необязателен. 
    
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ScCountProps](sccountprops.md)
  
[ScDupPropset](scduppropset.md)
  
[ScRelocNotifications](screlocnotifications.md)

