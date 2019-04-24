---
title: Имаписуппортжетмемаллокраутинес
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 680fd16771b62d705808a04d768115a076e54750
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316564"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получение адресов функций выделения и освобождения памяти MAPI ([мапиаллокатебуффер](mapiallocatebuffer.md), [мапиаллокатеморе](mapiallocatemore.md)и [мапифрибуффер](mapifreebuffer.md)).
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>Параметры

 _Лппаллокатебуффер_
  
> вышли Указатель на указатель на функцию **мапиаллокатебуффер** . **Мапиаллокатебуффер** выделяет память. 
    
 _Лппаллокатеморе_
  
> вышли Указатель на указатель на функцию **мапиаллокатеморе** . **Мапиаллокатеморе** выделяет дополнительную память для памяти, которая была изначально выделена с помощью **мапиаллокатебуффер**.
    
 _Лппфрибуффер_
  
> вышли Указатель на указатель на функцию **мапифрибуффер** . **Мапифрибуффер** освобождает память. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Адреса функции были успешно возвращены.
    
## <a name="remarks"></a>Замечания

Метод **имаписуппорт:: жетмемаллокраутинес** реализован для всех объектов поддержки. Поставщики услуг вызывают **жетмемаллокраутинес** для получения адресов трех функций выделения памяти, которые передаются в функцию инициализации ( [абпровидеринит](abproviderinit.md), [мспровидеринит](msproviderinit.md)или [ксппровидеринит](xpproviderinit.md)). 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

