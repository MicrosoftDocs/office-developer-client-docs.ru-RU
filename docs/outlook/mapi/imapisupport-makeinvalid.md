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
ms.openlocfilehash: 84e87f8a8d3c419afc4b86e200aeaba57e6a85f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427495"
---
# <a name="imapisupportmakeinvalid"></a>IMAPISupport::MakeInvalid

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Пометка объекта как непригодного для 2013 г.
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> Зарезервировано; должно быть нулем.
    
 _lpObject_
  
> [in] Указатель на объект, который необходимо сделать недействительным. Интерфейс объекта должен быть производным от **IUnknown**.
    
 _ulRefCount_
  
> [in] Настоящее количество ссылок объекта.
    
 _cMethods_
  
> [in] Количество методов в vtable объекта.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект успешно помечен как непригодный для 2013.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::MakeInvalid** реализован для всех объектов поддержки. Недопустимый объект должен быть производным от интерфейса **IUnknown** или интерфейса, производного от **IUnknown**.
  
 **MakeInvalid** пометит объект как непригодный для работы, заменив его vtable на загую vtable аналогичного размера, в котором методы **IUnknown::AddRef** и **IUnknown::Release** выполняются ожидаемым образом. Однако любые другие методы не удастся, возвращая значение MAPI_E_INVALID_OBJECT. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Поставщики услуг и службы сообщений обычно **звонят на makeInvalid** во время завершения работы. Однако **MakeInvalid** может быть вызван в любое время. Например, если клиент отпускает объект, не отпуская некоторые его подобекты, можно вызвать **MakeInvalid** немедленно, чтобы освободить эти подпроекты. 
  
Необходимо владеть объектом, который вы попытались сделать недействительным. Он должен иметь длину не менее 16 т и иметь по крайней мере три метода в своей вести. 
  
Можно вызвать **MakeInvalid,** а затем выполнить любые работы по отключению, такие как удаление связанных структур данных, которые обычно выполняются во время выпуска объекта. Код для поддержки объекта не должен храниться в памяти, так как MAPI освобождает память, вызывая [MAPIFreeBuffer,](mapifreebuffer.md) а затем освобождает объект. Вы можете освободить ресурсы, вызвать **MakeInvalid,** а затем игнорировать недопустимый объект. 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

