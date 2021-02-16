---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9a5f8b44f9d795282ccfd61fd32a306c5478ed21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416239"
---
# <a name="msproviderinit"></a>MSProviderInit

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Инициализирует поставщика для работы с хранилищем сообщений.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Реализовано в:  <br/> |Поставщики store сообщений  <br/> |
|Вызывающая сторона:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT MSProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPMSPROVIDER FAR * lppMSProvider
);
```

## <a name="parameters"></a>Параметры

 _hInstance_
  
> [in] Экземпляр библиотеки динамической ссылки поставщика хранения сообщений (DLL), используемой MAPI при его связи. 
    
 _lpMalloc_
  
> [in] Указатель на объект-память для размещения интерфейса OLE **IMalloc.** Поставщику хранилище сообщений может потребоваться использовать этот метод выделения при работе с определенными интерфейсами, такими как **IStream.** 
    
 _lpAllocateBuffer_
  
> [in] Указатель на [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) которая используется для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на [функцию MAPIAllocateMore,](mapiallocatemore.md) которая используется для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на [функцию MAPIFreeBuffer,](mapifreebuffer.md) которая используется для освободить память. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов. Можно установить следующий флаг:
    
MAPI_NT_SERVICE 
  
> Поставщик загружается в контексте службы Windows— особого типа процесса без доступа к пользовательскому интерфейсу. 
    
 _ulMAPIVer_
  
> [in] Номер версии интерфейса поставщика услуг (SPI), который использует MAPI. Номер текущей версии см. в файле заголовок Mapispi.h. 
    
 _lpulProviderVer_
  
> [out] Указатель на номер версии SPI, который использует этот поставщик хранилище сообщений. 
    
 _lppMSProvider_
  
> [out] Указатель на указатель на инициализированный объект поставщика хранения сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_VERSION 
  
> Версия SPI, используемая MAPI, несовместима с SPI, используемым этим поставщиком.
    
## <a name="remarks"></a>Примечания

MAPI вызывает функцию точки входа **MSProviderInit** для инициализации поставщика магазина сообщений после входа клиента. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщик точки входа должен реализовать **MSProviderInit** в DLL поставщика. Реализация должна быть основана на прототипе функции **MSPROVIDERINIT,** также указанном в MAPISPI.H. MAPI определяет **MSPROVIDERINIT** для использования стандартного типа вызова инициализации MAPI STDMAPIINITCALLTYPE, что приводит к следуют соглашению о вызовах CDECL **msProviderInit.** Преимуществом CDECL является возможность попытки вызова, даже если количество параметров вызова не соответствует числу заданных параметров. 
  
Поставщик может быть инициализирован несколько раз в результате одновременного использования нескольких профилей или появления в одном профиле более одного раза. Поскольку объект поставщика содержит контекст, **MSProviderInit** должен возвращать разные объекты поставщика в  _lppMSProvider_ для каждой инициализации даже для нескольких инициализации в одном процессе. 
  
DLL поставщика не следует связывать с Mapix.dll. Вместо этого он должен использовать эти указатели для выделения памяти или распределения памяти. 
  
Поставщик store сообщений должен использовать функции, на которые указывают  _lpAllocateBuffer,_  _lpAllocateMore_ и  _lpFreeBuffer_ для выделения и распределения памяти. В частности, поставщик должен использовать эти функции для выделения памяти для использования клиентских приложений при вызове интерфейсов объектов, таких как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). Если поставщик также ожидает использовать память OLE, он должен вызвать метод **IUnknown::AddRef** объекта allocator, на который указывает параметр _lpMalloc._ 
  
Дополнительные сведения о написании **MSProviderInit** см. в подпрограмме ["Загрузка поставщиков store сообщений".](loading-message-store-providers.md) Дополнительные сведения о функциях точек входа см. в [реализации функции](implementing-a-service-provider-entry-point-function.md)точки входа поставщика услуг. 
  
## <a name="see-also"></a>См. также



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

