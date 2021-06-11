---
title: XPProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.XPProviderInit
api_type:
- COM
ms.assetid: df6eacf4-1cf9-4c25-806f-f87c38dad597
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428538"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Инициализирует поставщика транспорта для работы.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Реализовано в:  <br/> |Поставщики транспорта  <br/> |
|Вызывающая сторона:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT XPProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPXPPROVIDER FAR * lppXPProvider
);
```

## <a name="parameters"></a>Parameters

 _hInstance_
  
> [in] Экземпляр библиотеки динамических ссылок поставщика транспорта (DLL), используемой MAPI при загрузке DLL.
    
 _lpMalloc_
  
> [in] Указатель на объект-аллигатор памяти, подвергая обнажает интерфейс OLE **IMalloc.** Поставщику транспорта может потребоваться использовать этот метод выделения при работе с определенными интерфейсами, такими как **IStream.** 
    
 _lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на функцию [MAPIAllocateMore,](mapiallocatemore.md) которая будет использоваться для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer,](mapifreebuffer.md) которая будет использоваться для бесплатной памяти. 
    
 _ulFlags_
  
> [in] Bitmask флагов. Можно установить следующий флаг:
    
MAPI_NT_SERVICE 
  
> Поставщик загружается в контексте службы Windows, особого типа процесса без доступа к любому пользовательскому интерфейсу. 
    
 _ulMAPIVer_
  
> [in] Номер версии интерфейса поставщика услуг (SPI), который Mapi.dll использует. Для текущего номера версии см. файл заголовки Mapispi.h. 
    
 _lpulProviderVer_
  
> [вышел] Указатель на номер версии SPI, который использует этот поставщик транспорта. 
    
 _lppXPProvider_
  
> [вышел] Указатель на указатель на инициализированный объект поставщика транспорта.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_VERSION 
  
> Версия SPI, используемая MAPI, не совместима с spi, используемым этим поставщиком.
    
## <a name="remarks"></a>Примечания

MAPI вызывает функцию точки входа **XPProviderInit** для инициализации поставщика транспорта после логотипа клиента. **XPProviderInit** вызван один раз для каждого поставщика транспорта, указанного в профиле клиента. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщик транспорта должен реализовать **XPProviderInit** в качестве функции точки входа в DLL поставщика. Реализация должна основываться на прототипе **функции XPPROVIDERINIT,** также указанном в Mapispi.h. MAPI определяет **XPPROVIDERINIT** для использования стандартного типа вызовов инициализации MAPI STDMAPIINITCALLTYPE, из-за чего **XPProviderInit** следует конвенции вызова CDECL. ПреимуществоМ CDECL является то, что вызовы можно предпринять даже в том случае, если количество параметров вызова не соответствует количеству заданных параметров. 
  
Поставщик может быть инициализирован несколько раз в результате появления в нескольких профилях одновременного использования или более одного раза в одном профиле. Так как объект поставщика содержит контекст, **XPProviderInit** должен возвращать другой объект поставщика  _в lppXPProvider_ для каждой инициализации даже для нескольких инициализации в одном и том же процессе. 
  
Поставщик транспорта должен использовать функции, на которые указывает  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ для большинства распределений памяти и deallocation. В частности, поставщик должен использовать эти функции для выделения памяти для использования в клиентских приложениях при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). Если поставщик также рассчитывает использовать аллигатор памяти OLE, он должен вызвать **метод IUnknown::AddRef** объекта-аллигатора, на который указывает параметр _lpMalloc._ 
  
Дополнительные сведения о **написании XPProviderInit** см. в [инициализации поставщика транспорта.](initializing-the-transport-provider.md) Дополнительные сведения о функциях точек входа см. в см. в нем [Implementing a Service Provider Entry Point Function.](implementing-a-service-provider-entry-point-function.md) 
  
## <a name="see-also"></a>См. также



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

