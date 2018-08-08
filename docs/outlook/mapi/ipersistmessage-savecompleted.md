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
ms.openlocfilehash: 7a82ce9a46017993adfc6c4c755b6c97b847e579
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809502"
---
# <a name="ipersistmessagesavecompleted"></a>IPersistMessage::SaveCompleted

**Относится к**: Outlook 
  
Уведомляет формы, которая сохранения завершения операции. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Параметры

_pMessage_
  
> [in] Указатель на только что сохраненный сообщения.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Уведомление успешно.
    
E_INVALIDARG 
  
> Параметр _pMessage_ имеет значение NULL и форма находится в состоянии [HandsOffFromNormal](handsofffromnormal-state.md) или [HandsOffAfterSave](handsoffaftersave-state.md) . 
    
ЗНАЧЕНИЕ E_UNEXPECTED 
  
> Форма не является одним из следующих состояний:
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Замечания

Метод **IPersistMessage::SaveCompleted** вызывается средством просмотра формы для уведомления формы, в которой были сохранены все ожидающие изменения. **SaveCompleted** должны вызывать только в том случае, когда форма находится в одном из следующих состояний: 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Существует несколько возможных действий, которые могут выполнять метод **SaveCompleted** , в зависимости от того, какие сообщения содержит параметр-указатель и состояния сообщение находится в. Тем не менее при успешной действие, которое всегда сохраните текущее состояние сообщения, параметр _pMessage_ и переход на новые формы в состояние [Normal](normal-state.md) . 
  
В следующей таблице описываются условия, которые влияют на действия, которые необходимо выполнять в реализации **SaveCompleted**.
  
|**Условие**|**Действие**|
|:-----|:-----|
|Параметр _pMessage_ имеет значение NULL, и параметр _fSameAsLoad_ метода [IPersistMessage::Save](ipersistmessage-save.md) задано значение TRUE.  <br/> |Вызовите метод [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) всем зарегистрированным пользователям, пометить форму как чистая, а возвращаемое значение S_OK.  <br/> |
|Параметр _pMessage_ имеет значение NULL, и параметр _fSameAsLoad_ метода **IPersistMessage::Save** задано значение FALSE.  <br/> |Возвращает значение S_OK.  <br/> |
|Форма находится в состоянии HandsOffFromNormal.  <br/> |Освобождение сообщения, текущий и замените указывает параметр _pMessage_ сообщение. Вызовите метод [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) замены сообщения и возвращает значение S_OK.  <br/> |
|Форма находится в состоянии HandsOffAfterSave.  <br/> |Вызовите метод **IMAPIViewAdviseSink::OnSaved** всем зарегистрированным пользователям, пометить форму как чистая, а возвращаемое значение S_OK.  <br/> |
|Форма находится в состоянии [NoScribble](noscribble-state.md) .  <br/> |Освобождение сообщения, текущий и замените сообщение, которое указывает _pMessage_. Вызов метода **IUnknown::AddRef** замены сообщения. Вызовите метод **IMAPIViewAdviseSink::OnSaved** всем зарегистрированным пользователям, пометить форму как чистая, а возвращаемое значение S_OK.  <br/> |
|Форма находится в одном из состояний HandsOff и параметр _pMessage_ имеет значение NULL.  <br/> |Возвращает E_INVALIDARG.  <br/> |
|Форма находится в состоянии от одного из состояний HandsOff или NoScribble.  <br/> |Возвращает значение E_UNEXPECTED.  <br/> |
   
Дополнительные сведения о сохранении объектов хранилища [IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx) или [IPersistFile::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx) методов см. 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Состояния форм](form-states.md)


[IPersistStorage::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersiststorage_savecompleted%28Office.15%29.aspx)
  
[IPersistFile::SaveCompleted](http://msdn.microsoft.com/library/_com_ipersistfile_savecompleted%28Office.15%29.aspx)

