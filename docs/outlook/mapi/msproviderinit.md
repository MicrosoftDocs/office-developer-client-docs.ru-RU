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
ms.openlocfilehash: cf1febe89c49b29cdfaf8d27760c4fb27b4c4990
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810032"
---
# <a name="msproviderinit"></a>MSProviderInit

  
  
**Относится к**: Outlook 
  
Инициализирует поставщика хранилища сообщений для операции.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Реализованный:  <br/> |Поставщики хранилища сообщений  <br/> |
|Вызывается:  <br/> |MAPI  <br/> |
   
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
  
> [in] Экземпляр сообщения хранилища поставщика динамической библиотеки (DLL), который используется MAPI, когда она связана. 
    
 _lpMalloc_
  
> [in] Указатель на объект распределителя памяти, предоставление интерфейса OLE **IMalloc** . Поставщик хранения сообщений может потребоваться использовать этот метод для распределения при работе с определенных интерфейсов, таких как **IStream**. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти. 
    
 _lpAllocateMore_
  
> [in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , которые будут использоваться для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти. 
    
 _ulFlags_
  
> [in] Битовая маска флаги. Можно задать следующий флаг:
    
MAPI_NT_SERVICE 
  
> Поставщик загружается в контексте службы Windows, особый тип процесса без доступа к любой пользовательский интерфейс. 
    
 _ulMAPIVer_
  
> [in] Номер версии поставщика службы интерфейса (SPI), который использует MAPI. Файл заголовка Mapispi.h текущий номер версии, см. 
    
 _lpulProviderVer_
  
> [out] Указатель на номер версии индекс параметров безопасности, которая использует этот поставщик хранения сообщений. 
    
 _lppMSProvider_
  
> [out] Указатель на указатель на объект поставщика хранилища инициализированную сообщения.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_VERSION 
  
> Версия SPI, используемые MAPI не совместимый с индекс параметров безопасности, используемые этим поставщиком.
    
## <a name="remarks"></a>Замечания

MAPI вызывает функцию точки входа **MSProviderInit** для инициализации поставщика хранилища сообщений после входа клиента. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщик хранения сообщений необходимо реализовать **MSProviderInit** как функцию точки входа в DLL поставщика. Реализация должны быть основаны на прототип функции **MSPROVIDERINIT** также указано в MAPISPI. З. MAPI определяет **MSPROVIDERINIT** для использования типа стандартный вызова инициализации MAPI, STDMAPIINITCALLTYPE, что активирует **MSProviderInit** необходимо выполнить соглашение о вызовах CDECL. Преимуществом CDECL — даже в том случае, если число вызовов параметров не соответствует количество определенных параметров может выполняться звонки. 
  
Поставщик может быть инициализирован несколько раз, из-за изображения которых появляются в несколько профилей в одновременное использование или отображение более одного раза в одном профиле. Поскольку объект поставщика содержит контекста, **MSProviderInit** необходимо возвратить объект другого поставщика в _lppMSProvider_ для каждой инициализации, даже для нескольких инициализации в одном процессе. 
  
Библиотека поставщика не должны быть связаны с Mapix.dll. Вместо этого следует использовать эти указатели для выделения памяти или освобождение. 
  
Поставщик хранения сообщений следует использовать функции, на который указывает _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ для большинства выделение и освобождение памяти. В частности поставщик должен использовать эти функции для выделения памяти для использования с клиентскими приложениями при вызове интерфейсы объекта, такие как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). Если поставщик также требуется для использования распределителя памяти OLE, он должен вызвать метод **IUnknown::AddRef** распределителя объект, указанный в параметре _lpMalloc_ . 
  
Дополнительные сведения о написании **MSProviderInit**можно [Загрузка поставщиков хранилища сообщений](loading-message-store-providers.md). Дополнительные сведения о функциях точки входа [реализации функции выберите запись службы поставщика](implementing-a-service-provider-entry-point-function.md)см. 
  
## <a name="see-also"></a>См. также



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

