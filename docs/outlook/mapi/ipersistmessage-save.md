---
title: IPersistMessageSave
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.Save
api_type:
- COM
ms.assetid: 17875c13-f55b-4538-ac6f-c020281c3175
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fa3f1d6339000fcc53e0ee22dafec4362e65ca7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309620"
---
# <a name="ipersistmessagesave"></a>IPersistMessage::Save

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сохраняет измененную форму обратно в сообщение, из которого она была загружена или создана.
  
```cpp
HRESULT Save(
  LPMESSAGE pMessage,
  ULONG fSameAsLoad
);
```

## <a name="parameters"></a>Параметры

 _pMessage_
  
> [in] Указатель на сообщение.
    
 _fSameAsLoad_
  
> [in] TRUE указывает, что сообщение, на которое указывает  _pMessage,_ — это сообщение, из которого была загружена или создана форма; в противном случае false. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Форма успешно сохранена.
    
## <a name="remarks"></a>Примечания

Посетители форм вызовите метод **IPersistMessage::Save,** чтобы сохранить измененную форму обратно в сообщение, из которого она была загружена или создана. 
  
 **Сохранение** должно быть вызвано только в том случае, если форма находится в [обычном состоянии.](normal-state.md) 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Не фиксировать сохраненные изменения; Зафиксировать изменения может только вызываемая. Никогда не внося изменений в свойства, принадлежащие  сообщению формы, за исключением вызова "Сохранить". 
  
Если  _для fSameAsLoad установлено_ true, изменения можно сохранить в существующем сообщении формы. Если _для fSameAsLoad_ установлено false, перед выполнением сохранения необходимо скопировать все свойства из исходного сообщения в сообщение, на которое указывает _pMessage._ Используйте метод [IMAPIProp::CopyTo](imapiprop-copyto.md) исходного сообщения для копирования свойств. 
  
После копирования всех свойств введите состояние [NoScribble.](noscribble-state.md) Если ошибки не возникают, S_OK. В противном случае возвратим ошибку из неудачного действия. 
  
Если **при** сохранения форма находится в любом состоянии, кроме обычного, возвращается E_UNEXPECTED. 
  
Дополнительные сведения о сохранении объектов хранилища см. в документации по методам [IPersistStorage.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Состояния форм](form-states.md)

