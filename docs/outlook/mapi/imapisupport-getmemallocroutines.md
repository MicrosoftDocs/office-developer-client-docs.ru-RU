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
ms.openlocfilehash: 782c04d05ea5cea811784b031e8a118a9c08cbb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809134"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**Относится к**: Outlook 
  
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

