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
ms.openlocfilehash: 38b60180ae7c417bf34998e72f96b353ace02859
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592537"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Инициализирует поставщика транспорта для операции.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Реализованный:  <br/> |Поставщиками транспорта  <br/> |
|Вызывается:  <br/> |MAPI  <br/> |
   
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
  
> [in] Экземпляр поставщика транспорта динамической библиотеки (DLL), MAPI, используемой при загрузке DLL.
    
 _lpMalloc_
  
> [in] Указатель на объект распределителя памяти, предоставление интерфейса OLE **IMalloc** . Поставщика транспорта может потребоваться использовать этот метод для распределения при работе с определенных интерфейсов, таких как **IStream**. 
    
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
  
> [in] Номер версии поставщика службы интерфейса (SPI), который использует Mapi.dll. Файл заголовка Mapispi.h текущий номер версии, см. 
    
 _lpulProviderVer_
  
> [out] Указатель на номер версии индекс параметров безопасности, которая использует этот поставщик транспорта. 
    
 _lppXPProvider_
  
> [out] Указатель на указатель на объект поставщика инициализированную транспорта.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_VERSION 
  
> Версия SPI, используемые MAPI не совместимый с индекс параметров безопасности, используемые этим поставщиком.
    
## <a name="remarks"></a>Замечания

MAPI вызывает функцию точки входа **XPProviderInit** для инициализации поставщика транспорта после входа клиента. **XPProviderInit** вызывается один раз для каждого поставщика транспорта, указанного в профиле клиента. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщика транспорта необходимо реализовать **XPProviderInit** как функцию точки входа в DLL поставщика. Реализация должны быть основаны на прототип функции **XPPROVIDERINIT** также указано в Mapispi.h. MAPI определяет **XPPROVIDERINIT** для использования типа стандартный вызова инициализации MAPI, STDMAPIINITCALLTYPE, что активирует **XPProviderInit** необходимо выполнить соглашение о вызовах CDECL. Преимуществом CDECL — даже в том случае, если число вызовов параметров не соответствует количество определенных параметров может выполняться звонки. 
  
Поставщик может быть инициализирован несколько раз из-за изображения которых появляются в несколько профилей в одновременное использование или отображение более одного раза в одном профиле. Поскольку объект поставщика содержит контекста, **XPProviderInit** необходимо возвратить объект другого поставщика в _lppXPProvider_ для каждой инициализации, даже для нескольких инициализации в одном процессе. 
  
Поставщика транспорта должно использовать функции, на который указывает _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ для большинства выделение и освобождение памяти. В частности поставщик должен использовать эти функции для выделения памяти для использования с клиентскими приложениями при вызове интерфейсы объекта, такие как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). Если поставщик также требуется для использования распределителя памяти OLE, он должен вызвать метод **IUnknown::AddRef** распределителя объект, указанный в параметре _lpMalloc_ . 
  
Дополнительные сведения о создании **XPProviderInit**можно [инициализации поставщика транспорта](initializing-the-transport-provider.md). Дополнительные сведения о функциях точки входа [реализации функции выберите запись службы поставщика](implementing-a-service-provider-entry-point-function.md)см. 
  
## <a name="see-also"></a>См. также



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

