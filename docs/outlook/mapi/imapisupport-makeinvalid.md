---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 595d5fdba28634b038838921102d3125135452a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809128"
---
# <a name="imapisupportmakeinvalid"></a>IMAPISupport::MakeInvalid

  
  
**Относится к**: Outlook 
  
Помечает объект недоступным.
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> Зарезервировано; должно быть равно нулю.
    
 _lpObject_
  
> [in] Указатель на объект становятся недействительными. Интерфейс объекта должен быть производным от **IUnknown**.
    
 _ulRefCount_
  
> [in] Объект присутствует счетчик ссылок.
    
 _cMethods_
  
> [in] Число методов в vtable объекта.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Успешно помечено как могут использовать объект.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::MakeInvalid** применяется для всех объектов поддержки. Объект становятся недействительными должен быть производным от **IUnknown** интерфейс или из интерфейса, производным от **IUnknown**.
  
 **MakeInvalid** помечает объект недоступным, заменив vtable объекта vtable заглушка следующего размера, выполнение методов **IUnknown::AddRef** и **функции IUnknown::Release** , как ожидалось. Тем не менее другие методы не удается, возврат значения MAPI_E_INVALID_OBJECT. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Поставщики службы и службы сообщений обычно вызов **MakeInvalid** во время завершения работы. Тем не менее **MakeInvalid** может быть вызван в любое время. К примеру клиент освобождает объект без освобождения некоторые из ее вложенных объектов, можно вызвать **MakeInvalid** непосредственно к выпуску этих вложенных. 
  
Необходимо быть владельцем объекта, который предпринимается попытка объявить недействительным. Он должен быть менее 16 байт и иметь по крайней мере три метода в его vtable. 
  
Можно вызвать **MakeInvalid** и затем выполнить любые действия, завершение работы, такие как пропуск структур данных, связанного, которая обычно выполняется во время выпуска объекта. Код для поддержки объекта не требуется их хранения в памяти, так как MAPI освобождает память, вызвав [MAPIFreeBuffer](mapifreebuffer.md) , а затем освобождает объект. Можно освободить ресурсы, вызвать **MakeInvalid**и игнорировать недействительным объекта. 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

