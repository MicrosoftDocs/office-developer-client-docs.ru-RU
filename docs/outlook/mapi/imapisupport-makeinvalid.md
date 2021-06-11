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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Пометит объект как непригодный.
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> Зарезервировано; должно быть нулевой.
    
 _lpObject_
  
> [in] Указатель на объект, который будет признан недействительным. Интерфейс объекта должен быть получен из **IUnknown**.
    
 _ulRefCount_
  
> [in] Настоящее количество ссылок объекта.
    
 _cMethods_
  
> [in] Количество методов в vtable объекта.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Объект был успешно помечен как непригодный для пользоваемых объектов.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::MakeInvalid** реализован для всех объектов поддержки. Объект, который должен быть признан недействительным, должен быть получен из **интерфейса IUnknown** или интерфейса, полученного из **IUnknown.**
  
 **MakeInvalid** отмечает объект как непригодный для работы, заменив vtable объекта на загребный vtable аналогичного размера, в котором методы **IUnknown::AddRef** и **IUnknown::Release** выполняются как ожидалось. Однако любые другие методы сбой, возвращая значение MAPI_E_INVALID_OBJECT. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Поставщики услуг и службы сообщений обычно звонят **в MakeInvalid** во время остановки. Однако **MakeInvalid** можно назвать в любое время. Например, если клиент выпускает объект, не выпуская некоторые из его субобектов, вы можете немедленно вызвать **MakeInvalid,** чтобы освободить эти субобпроекты. 
  
Вы должны владеть объектом, который вы попытаете признать недействительным. Она должна быть длиной не менее 16 bytes и иметь по крайней мере три метода в ее vtable. 
  
Можно вызвать **MakeInvalid** и выполнить любые работы по остановке, например удаление связанных структур данных, которые обычно выполняются во время выпуска объекта. Код для поддержки объекта не должен храниться в памяти, так как MAPI освобождает память, вызывая [MAPIFreeBuffer,](mapifreebuffer.md) а затем освобождает объект. Можно освободить ресурсы, вызвать **MakeInvalid,** а затем игнорировать недействительный объект. 
  
## <a name="see-also"></a>См. также



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

