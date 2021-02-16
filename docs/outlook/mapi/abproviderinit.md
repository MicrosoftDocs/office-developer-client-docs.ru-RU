---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: acec07df0b72685cf9ec6b21499c730b72f58c59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428286"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
Инициализирует поставщика адресной книги для работы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Реализовано в:  <br/> |Поставщики адресных книг  <br/> |
|Вызывающая сторона:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT ABProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPABPROVIDER FAR * lppABProvider
);
```

## <a name="parameters"></a>Параметры

 _hInstance_
  
> [in] Экземпляр библиотеки динамической ссылки (DLL) поставщика адресной книги, используемой MAPI при его связи. 
    
 _lpMalloc_
  
> [in] Указатель на объект-память для размещения интерфейса OLE **IMalloc.** Поставщику адресной книги может потребоваться использовать этот метод выделения при работе с определенными интерфейсами, такими как **IStream.** 
    
 _lpAllocateBuffer_
  
> [in] Указатель на функцию [MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться при необходимости MAPI для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на функцию [MAPIAllocateMore,](mapiallocatemore.md) которая будет использоваться при необходимости MAPI для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая будет использоваться при необходимости MAPI для освободить память. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов. Можно установить следующий флаг:
    
MAPI_NT_SERVICE 
  
> Поставщик загружается в контексте службы Windows— особого типа процесса без доступа к пользовательскому интерфейсу. 
    
 _ulMAPIVer_
  
> [in] Номер версии интерфейса поставщика услуг (SPI), который MAPI.DLL. Номер текущей версии см. в MAPISPI. Файл h-загона. 
    
 _lpulProviderVer_
  
> [out] Указатель на номер версии SPI, который использует этот поставщик адресной книги. 
    
 _lppABProvider_
  
> [out] Указатель на указатель на инициализированный объект поставщика адресной книги.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_VERSION 
  
> Версия SPI, используемая MAPI, несовместима с SPI, используемым этим поставщиком.
    
## <a name="remarks"></a>Примечания

MAPI вызывает функцию точки входа **ABProviderInit** для инициализации поставщика адресной книги после входа клиента. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщик адресной книги должен реализовать **ABProviderInit** в качестве функции точки входа в DLL поставщика. Реализация должна быть основана на прототипе **функции ABPROVIDERINIT,** также указанном в MAPISPI.H. MAPI определяет **ABPROVIDERINIT** для использования стандартного типа вызова инициализации MAPI STDMAPIINITCALLTYPE, что приводит к следуют соглашению о вызовах CDECL для **ABProviderInit.** 
  
Поставщик может быть инициализирован несколько раз в результате одновременного использования нескольких профилей или появления в одном профиле более одного раза. Так как объект поставщика содержит контекст, **ABProviderInit** должен возвращать разные объекты поставщика в  _lppABProvider_ для каждой инициализации даже для нескольких инициализации в одном процессе. 
  
Поставщик адресной книги должен использовать функции, на которые указывают  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ для выделения и распределения памяти. В частности, поставщик должен использовать эти функции для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). Если поставщик также ожидает использовать память OLE, он должен вызвать метод **IUnknown::AddRef** объекта allocator, на который указывает параметр _lpMalloc._ 
  
Дополнительные сведения о написании **ABProviderInit** см. в реализации функции точки входа поставщика [адресной книги.](implementing-an-address-book-provider-entry-point-function.md) Дополнительные сведения о функциях точек входа см. в [реализации функции](implementing-a-service-provider-entry-point-function.md)точки входа поставщика услуг. 
  
## <a name="see-also"></a>См. также

- [IABProvider : IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

