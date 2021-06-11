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
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _hInstance_
  
> [in] Экземпляр библиотеки динамических ссылок поставщика адресных книг (DLL), используемой MAPI при его подключении. 
    
 _lpMalloc_
  
> [in] Указатель на объект-аллигатор памяти, подвергая обнажает интерфейс OLE **IMalloc.** Поставщику адресных книг может потребоваться использовать этот метод выделения при работе с определенными интерфейсами, такими как **IStream.** 
    
 _lpAllocateBuffer_
  
> [in] Указатель на функцию [MAPIAllocateBuffer,](mapiallocatebuffer.md) которая будет использоваться при необходимости MAPI для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на функцию [MAPIAllocateMore,](mapiallocatemore.md) которая будет использоваться, если это требуется MAPI для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer,](mapifreebuffer.md) которая будет использоваться, если это требуется MAPI для бесплатной памяти. 
    
 _ulFlags_
  
> [in] Bitmask флагов. Можно установить следующий флаг:
    
MAPI_NT_SERVICE 
  
> Поставщик загружается в контексте службы Windows, особого типа процесса без доступа к любому пользовательскому интерфейсу. 
    
 _ulMAPIVer_
  
> [in] Номер версии интерфейса поставщика услуг (SPI), который MAPI.DLL использует. Для текущего номера версии см. MAPISPI. Файл заглавной папки H. 
    
 _lpulProviderVer_
  
> [вышел] Указатель на номер версии SPI, который использует этот поставщик адресных книг. 
    
 _lppABProvider_
  
> [вышел] Указатель на указатель на инициализированный объект поставщика адресной книги.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_VERSION 
  
> Версия SPI, используемая MAPI, не совместима с spi, используемым этим поставщиком.
    
## <a name="remarks"></a>Примечания

MAPI вызывает функцию точки входа **ABProviderInit** для инициализации поставщика адресной книги после логотипа клиента. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщик адресных книг должен реализовать **ABProviderInit** в качестве функции точки входа в DLL поставщика. Реализация должна основываться на прототипе **функции ABPROVIDERINIT,** также указанном в MAPISPI.H. MAPI определяет **ABPROVIDERINIT** для использования стандартного типа вызовов инициализации MAPI STDMAPIINITCALLTYPE, из-за чего **ABProviderInit** следует конвенции вызова CDECL. 
  
Поставщик может быть инициализирован несколько раз в результате появления в нескольких профилях одновременного использования или более одного раза в одном профиле. Так как объект поставщика содержит контекст, **ABProviderInit** должен возвращать другой объект поставщика в  _lppABProvider_ для каждой инициализации даже для нескольких инициализации в одном и том же процессе. 
  
Поставщик адресной книги должен использовать функции, на которые указывает  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ для большинства распределений памяти и распределения. В частности, поставщик должен использовать эти функции для выделения памяти для использования в клиентских приложениях при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). Если поставщик также рассчитывает использовать аллигатор памяти OLE, он должен вызвать **метод IUnknown::AddRef** объекта-аллигатора, на который указывает параметр _lpMalloc._ 
  
Дополнительные сведения о написании **ABProviderInit** см. в книге [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md). Дополнительные сведения о функциях точек входа см. в пункте [Реализация функции](implementing-a-service-provider-entry-point-function.md)точки входа поставщика услуг. 
  
## <a name="see-also"></a>См. также

- [IABProvider : IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

