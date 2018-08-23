---
title: IMAPISupportGetMemAllocRoutines
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
ms.openlocfilehash: c3ec99e4e284ca2cdc4fba8fcf53a6c5741594cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577816"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Получает адреса MAPI памяти выделение и освобождение функции ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md)).
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>Параметры

 _lppAllocateBuffer_
  
> [out] Указатель на указатель на функцию **MAPIAllocateBuffer** . **MAPIAllocateBuffer** выделение памяти. 
    
 _lppAllocateMore_
  
> [out] Указатель на указатель на функцию **MAPIAllocateMore** . **MAPIAllocateMore** выделяет дополнительную память для память, изначально выделенную с помощью **MAPIAllocateBuffer**.
    
 _lppFreeBuffer_
  
> [out] Указатель на указатель на функцию **MAPIFreeBuffer** . **MAPIFreeBuffer** освобождает память. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Функция адреса были успешно возвращен.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::GetMemAllocRoutines** применяется для всех объектов поддержки. Поставщики услуг вызов **GetMemAllocRoutines** для получения адреса функций выделения памяти, которые передаются в свои функции инициализации ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)или [XPProviderInit](xpproviderinit.md)). 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

