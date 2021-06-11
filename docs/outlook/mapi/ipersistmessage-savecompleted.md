---
title: IPersistMessageSaveCompleted
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.SaveCompleted
api_type:
- COM
ms.assetid: 83161011-90b4-49cb-9bcd-153a21a10977
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 021be209a2b2c891b668fa401500d6220619f9bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317138"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**Область применения**: Outlook 2013 | Outlook 2016 
  
Сообщает форму о том, что операция сохранения завершена. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Parameters

_pMessage_
  
> [in] Указатель на недавно сохраненное сообщение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление было успешным.
    
E_INVALIDARG 
  
> Параметр _pMessage_ — NULL, а форма находится в состоянии [HandsOffFromNormal](handsofffromnormal-state.md) или [HandsOffAfterSave.](handsoffaftersave-state.md) 
    
E_UNEXPECTED 
  
> Форма не находится в одном из следующих штатов:
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Примечания

Метод **IPersistMessage::SaveCompleted** вызван просмотром форм, чтобы уведомить форму о том, что все ожидающих изменений сохранены. **SaveCompleted** следует называть только в том случае, если форма находится в одном из следующих штатов: 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Существует несколько возможных действий, которые может выполнять метод **SaveCompleted,** в зависимости от того, что содержит параметр указателя сообщения и в каком состоянии находится сообщение. Однако при успешном действии всегда сохраните текущее состояние сообщения, на которое указывает параметр  _pMessage,_ и перенаправляем форму в [нормальное](normal-state.md) состояние. 
  
В следующей таблице описываются условия, влияющие на действия, которые необходимо принять при реализации **SaveCompleted.**
  
|**Условие**|**Действие**|
|:-----|:-----|
|Параметр  _pMessage_ — NULL, а  _параметр fSameAsLoad_ метода [IPersistMessage::Сохранить](ipersistmessage-save.md) задан для TRUE.  <br/> |Вызовите [метод IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) для всех зарегистрированных зрителей, пометить форму как чистую и S_OK.  <br/> |
|Параметр  _pMessage_ — NULL, а  _параметр fSameAsLoad_ метода **IPersistMessage::Сохранить** задан для FALSE.  <br/> |Возвращение S_OK.  <br/> |
|Форма находится в состоянии HandsOffFromNormal.  <br/> |Освободите текущее сообщение и замените его сообщением, на которое указывает параметр _pMessage._ Вызовите метод [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) и S_OK.  <br/> |
|Форма находится в состоянии HandsOffAfterSave.  <br/> |Вызовите **метод IMAPIViewAdviseSink::OnSaved** для всех зарегистрированных зрителей, пометить форму как чистую и S_OK.  <br/> |
|Форма находится в состоянии [NoScribble.](noscribble-state.md)  <br/> |Освободите текущее сообщение и замените его сообщением, на которое указывает _pMessage._ Вызов метода **IUnknown::AddRef** сообщения замены. Вызовите **метод IMAPIViewAdviseSink::OnSaved** для всех зарегистрированных зрителей, пометить форму как чистую и S_OK.  <br/> |
|Форма находится в одном из состояниях HandsOff, а параметр  _pMessage_ задан в NULL.  <br/> |Возвращение E_INVALIDARG.  <br/> |
|Форма находится в состоянии, помимо одного из состояния HandsOff или состояния NoScribble.  <br/> |Возвращение E_UNEXPECTED.  <br/> |
   
Дополнительные сведения о сохранении объектов хранения см. в документации по методам [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) или [IPersistFile::SaveCompleted.](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) 
  
## <a name="see-also"></a>См. также

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [Состояния форм](form-states.md)
