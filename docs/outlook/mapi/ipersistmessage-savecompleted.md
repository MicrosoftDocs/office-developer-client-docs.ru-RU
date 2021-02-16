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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Сообщает форме, что операция сохранения завершена. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Параметры

_pMessage_
  
> [in] Указатель на только что сохраненное сообщение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление успешно.
    
E_INVALIDARG 
  
> Параметр _pMessage_ имеет NULL, а форма находится в состоянии [HandsOffFromNormal](handsofffromnormal-state.md) или [HandsOffAfterSave.](handsoffaftersave-state.md) 
    
E_UNEXPECTED 
  
> Форма находится не в одном из следующих состояниях:
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Примечания

Метод **IPersistMessage::SaveCompleted** вызван просмотром формы, чтобы уведомить форму о том, что все ожидающих изменений сохранены. **SaveCompleted** следует использовать только в том случае, если форма находится в одном из следующих состояниях: 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Существует несколько возможных действий, которые может выполнять метод **SaveCompleted** в зависимости от того, что содержит параметр указателя сообщения и в каком состоянии находится сообщение. Однако при успешном действии всегда сохраняете текущее состояние сообщения, на которое указывает параметр  _pMessage,_ и переводите форму в [обычное](normal-state.md) состояние. 
  
В следующей таблице описываются условия, влияющие на действия, которые необходимо принять при реализации **SaveCompleted.**
  
|**Условие**|**Действие**|
|:-----|:-----|
|Параметр  _pMessage_ имеет NULL, а для параметра  _fSameAsLoad_ метода [IPersistMessage::Save](ipersistmessage-save.md) задано true.  <br/> |Вызовите метод [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) всех зарегистрированных пользователей, пометить форму как чистую и вернуть S_OK.  <br/> |
|Параметр  _pMessage_ имеет NULL, а для параметра  _fSameAsLoad_ метода **IPersistMessage::Save** задано false.  <br/> |Возврат S_OK.  <br/> |
|Форма находится в состоянии HandsOffFromNormal.  <br/> |Освободите текущее сообщение и замените его на сообщение, на которое указывает параметр _pMessage._ Вызовите метод [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) сообщения замены и S_OK.  <br/> |
|Форма находится в состоянии HandsOffAfterSave.  <br/> |Вызовите метод **IMAPIViewAdviseSink::OnSaved** всех зарегистрированных пользователей, пометить форму как чистую и вернуть S_OK.  <br/> |
|Форма находится в состоянии [NoScribble.](noscribble-state.md)  <br/> |Освободите текущее сообщение и замените его на сообщение, на которое указывает _pMessage._ Вызовите метод **IUnknown::AddRef** сообщения замены. Вызовите метод **IMAPIViewAdviseSink::OnSaved** всех зарегистрированных пользователей, пометить форму как чистую и вернуть S_OK.  <br/> |
|Форма находится в одном из состояния HandsOff, а для параметра  _pMessage_ задано NULL.  <br/> |Возврат E_INVALIDARG.  <br/> |
|Форма находится в состоянии, не относяном к одному из состояния handsOff или NoScribble.  <br/> |Возврат E_UNEXPECTED.  <br/> |
   
Дополнительные сведения о сохранении объектов хранилища см. в документации по методам [IPersistStorage::SaveCompleted](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) или [IPersistFile::SaveCompleted.](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) 
  
## <a name="see-also"></a>См. также

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [Состояния форм](form-states.md)
