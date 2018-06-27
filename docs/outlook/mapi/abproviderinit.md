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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 03375a11be3f6f128db5f6147c5fbe901d0a0fa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807990"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**Применимо к**: Outlook 
  
Инициализирует поставщика адресных книг для операции. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Реализованный:  <br/> |Поставщиками адресных книг  <br/> |
|Вызывается:  <br/> |MAPI  <br/> |
   
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
  
> [in] Экземпляр поставщик адресной книги динамической библиотеки (DLL), который используется MAPI, когда она связана. 
    
 _lpMalloc_
  
> [in] Указатель на объект распределителя памяти, предоставление интерфейса OLE **IMalloc** . Поставщик адресной книги может потребоваться использовать этот метод для распределения при работе с определенных интерфейсов, таких как **IStream**. 
    
 _lpAllocateBuffer_
  
> [in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) для использования где по MAPI требуется выделить память. 
    
 _lpAllocateMore_
  
> [in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) для использования где по MAPI требуется для выделения дополнительной памяти. 
    
 _lpFreeBuffer_
  
> [in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) для использования где по MAPI требуется свободной памяти. 
    
 _ulFlags_
  
> [in] Битовая маска флаги. Можно задать следующий флаг:
    
MAPI_NT_SERVICE 
  
> Поставщик загружается в контексте службы Windows, особый тип процесса без доступа к любой пользовательский интерфейс. 
    
 _ulMAPIVer_
  
> [in] Номер версии интерфейса поставщика службы (SPI), MAPI. Использует библиотеку DLL. Текущий номер версии в разделе MAPISPI. Файл заголовка. 
    
 _lpulProviderVer_
  
> [out] Указатель на номер версии индекс параметров безопасности, которая использует этот поставщик адресной книги. 
    
 _lppABProvider_
  
> [out] Указатель на указатель на объект поставщика инициализированную адресной книги.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������. 
    
MAPI_E_VERSION 
  
> Версия SPI, используемые MAPI не совместимый с индекс параметров безопасности, используемые этим поставщиком.
    
## <a name="remarks"></a>Замечания

MAPI вызывает функцию точки входа **ABProviderInit** для инициализации поставщика адресных книг после входа клиента. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Поставщик адресной книги необходимо реализовать **ABProviderInit** как функцию точки входа в DLL поставщика. Реализация должны быть основаны на прототип функции **ABPROVIDERINIT** также указано в MAPISPI. З. MAPI определяет **ABPROVIDERINIT** для использования типа стандартный вызова инициализации MAPI, STDMAPIINITCALLTYPE, что активирует **ABProviderInit** необходимо выполнить соглашение о вызовах CDECL. 
  
Поставщик может быть инициализирован несколько раз, из-за изображения которых появляются в несколько профилей в одновременное использование или отображение более одного раза в одном профиле. Поскольку объект поставщика содержит контекста, **ABProviderInit** необходимо возвратить объект другого поставщика в _lppABProvider_ для каждой инициализации, даже для нескольких инициализации в одном процессе. 
  
Поставщик адресной книги следует использовать функции, на который указывает _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ для большинства выделение и освобождение памяти. В частности поставщик должен использовать эти функции для выделения памяти для использования с клиентскими приложениями при вызове интерфейсы объекта, такие как [IMAPIProp::GetProps](imapiprop-getprops.md) и [IMAPITable::QueryRows](imapitable-queryrows.md). Если поставщик также требуется для использования распределителя памяти OLE, он должен вызвать метод **IUnknown::AddRef** распределителя объект, указанный в параметре _lpMalloc_ . 
  
Дополнительные сведения о создании **ABProviderInit** [Функцию адресной книги поставщика](implementing-an-address-book-provider-entry-point-function.md)см. Дополнительные сведения о функциях точки входа [реализации функции выберите запись службы поставщика](implementing-a-service-provider-entry-point-function.md)см. 
  
## <a name="see-also"></a>См. также

- [IABProvider: IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)
