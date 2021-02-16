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
ms.openlocfilehash: 680fd16771b62d705808a04d768115a076e54750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415539"
---
# <a name="imapisupportgetmemallocroutines"></a>IMAPISupport::GetMemAllocRoutines

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Извлекает адреса функций выделения памяти и распределения MAPI ([MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)и [MAPIFreeBuffer).](mapifreebuffer.md)
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a>Параметры

 _lppAllocateBuffer_
  
> [out] Указатель на указатель на функцию **MAPIAllocateBuffer.** **MAPIAllocateBuffer выделяет** память. 
    
 _lppAllocateMore_
  
> [out] Указатель на указатель на функцию **MAPIAllocateMore.** **MAPIAllocateMore** выделяет дополнительную память для памяти, изначально выделенной с помощью **MAPIAllocateBuffer.**
    
 _lppFreeBuffer_
  
> [out] Указатель на указатель на функцию **MAPIFreeBuffer.** **MAPIFreeBuffer** освободит память. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Адреса функций были успешно возвращены.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::GetMemAllocRoutines** реализован для всех объектов поддержки. Поставщики услуг звонят **GetMemAllocRoutines,** чтобы получить адреса трех функций выделения памяти, которые передаются в функцию инициализации [(ABProviderInit,](abproviderinit.md) [MSProviderInit](msproviderinit.md)или [XPProviderInit).](xpproviderinit.md) 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

