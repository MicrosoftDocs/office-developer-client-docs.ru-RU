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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Инициализирует поставщика транспорта для операции.
  
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

## <a name="parameters"></a>Параметры

 _hInstance_
  
> [in] Экземпляр библиотеки динамической ссылки поставщика транспорта (DLL), используемой MAPI при загрузке библиотеки DLL.
    
 _lpMalloc_
  
> [in] Указатель на объект-память для размещения интерфейса OLE **IMalloc.** Поставщику транспорта может потребоваться использовать этот метод выделения при работе с определенными интерфейсами, такими как **IStream.** 
    
 _lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на [функцию MAPIAllocateMore,](mapiallocatemore.md) которая используется для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов. Можно установить следующий флаг:
    
MAPI_NT_SERVICE 
  
> Поставщик загружается в контексте службы Windows — особого типа процесса без доступа к пользовательскому интерфейсу. 
    
 _ulMAPIVer_
  
> [in] Номер версии интерфейса поставщика услуг (SPI), который Mapi.dll. Номер текущей версии см. в файле заголовок Mapispi.h. 
    
 _lpulProviderVer_
  
> [out] Указатель на номер версии SPI, который использует этот поставщик транспорта. 
    
 _lppXPProvider_
  
> [out] Указатель на указатель на инициализированный объект поставщика транспорта.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_VERSION 
  
> Версия SPI, используемая MAPI, несовместима с SPI, используемым этим поставщиком.
    
## <a name="remarks"></a>Примечания

MAPI вызывает функцию точки входа **XPProviderInit** для инициализации поставщика транспорта после входа клиента. **XPProviderInit** будет вызван один раз для каждого поставщика транспорта, указанного в профиле клиента. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщик транспорта должен реализовать **XPProviderInit** в качестве функции точки входа в DLL поставщика. Реализация должна быть основана на прототипе **функции XPPROVIDERINIT,** который также указан в mapispi.h. MAPI определяет **XPPROVIDERINIT** для использования стандартного типа вызова инициализации MAPI, STDMAPIINITCALLTYPE, что приводит к следуют соглашению о вызовах **XPProviderInit** CDECL. Преимуществом CDECL является возможность попытки вызова, даже если количество параметров вызова не соответствует числу заданных параметров. 
  
Поставщик может быть инициализирован несколько раз в результате появления в нескольких профилях одновременного использования или появления более одного раза в одном профиле. Так как объект поставщика содержит контекст, **XPProviderInit** должен возвращать другой объект поставщика в  _lppXPProvider_ для каждой инициализации даже для нескольких инициализации в одном процессе. 
  
Поставщик транспорта должен использовать функции, на которые указывают  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ для выделения и распределения памяти. В частности, поставщик должен использовать эти функции для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). Если поставщик также ожидает использовать память OLE, он должен вызвать метод **IUnknown::AddRef** объекта allocator, на который указывает параметр _lpMalloc._ 
  
Дополнительные сведения о **написании XPProviderInit** см. в [инициализации поставщика транспорта.](initializing-the-transport-provider.md) Дополнительные сведения о функциях точек входа см. в [реализации функции](implementing-a-service-provider-entry-point-function.md)точки входа поставщика услуг. 
  
## <a name="see-also"></a>См. также



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

