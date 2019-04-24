---
title: Иперсистмессажесавекомплетед
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
  
Уведомляет форму о завершении операции сохранения. 
  
```cpp
HRESULT SaveCompleted(
  LPMESSAGE pMessage
);
```

## <a name="parameters"></a>Параметры

_Пмессаже_
  
> возврата Указатель на вновь сохраненное сообщение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Уведомление успешно установлено.
    
E_INVALIDARG 
  
> Параметр _пмессаже_ имеет значение null, а форма находится в состоянии [HandsOffFromNormal](handsofffromnormal-state.md) или [HandsOffAfterSave](handsoffaftersave-state.md) . 
    
Е_УНЕКСПЕКТЕД 
  
> Форма находится не в одном из следующих состояний:
    
   - HandsOffFromNormal
    
   - HandsOffAfterSave
    
   - [NoScribble](noscribble-state.md)
    
## <a name="remarks"></a>Замечания

Средство просмотра форм вызывает метод **иперсистмессаже:: савекомплетед** , чтобы уведомить форму о том, что все ожидающие изменения сохранены. **Савекомплетед** следует вызывать только в том случае, если форма находится в одном из следующих состояний: 
  
- HandsOffFromNormal
    
- HandsOffAfterSave
    
- NoScribble
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Существует несколько возможных действий, которые может выполнить метод **савекомплетед** в зависимости от того, что содержит параметр указателя сообщения, и в каком состоянии находится сообщение. Однако при успешном выполнении действия всегда сохраняйте текущее состояние сообщения, на которое указывает параметр _пмессаже_ , и переводит форму в [нормальное](normal-state.md) состояние. 
  
В следующей таблице описаны условия, которые влияют на действия, которые необходимо выполнить в реализации **савекомплетед**.
  
|**Условие**|**Действие**|
|:-----|:-----|
|Параметр _пмессаже_ имеет значение null, а параметр _Фсамеаслоад_ метода " [иперсистмессаже:: Save](ipersistmessage-save.md) " имеет значение true.  <br/> |ВыЗовите метод [имапивиевадвисесинк:: OnSave](imapiviewadvisesink-onsaved.md) для всех зарегистрированных средств просмотра, помечайте форму как Clean и ВОЗВРАТИТ значение S_OK.  <br/> |
|Параметр _пмессаже_ имеет значение null, а параметр _Фсамеаслоад_ метода " **иперсистмессаже:: Save** " имеет значение false.  <br/> |Возвращает значение S_OK.  <br/> |
|Форма находится в состоянии HandsOffFromNormal.  <br/> |Освободите текущее сообщение и замените его сообщением, на которое указывает параметр _пмессаже_ . ВыЗовите метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) сообщения rereplacement и ВОЗВРАТИТ значение S_OK.  <br/> |
|Форма находится в состоянии HandsOffAfterSave.  <br/> |ВыЗовите метод **имапивиевадвисесинк:: OnSave** для всех зарегистрированных средств просмотра, помечайте форму как Clean и ВОЗВРАТИТ значение S_OK.  <br/> |
|Форма находится в состоянии " [каракули](noscribble-state.md) ".  <br/> |Освободите текущее сообщение и замените его сообщением, на которое указывает _пмессаже_. ВыЗовите метод **IUnknown:: AddRef** для замещающего сообщения. ВыЗовите метод **имапивиевадвисесинк:: OnSave** для всех зарегистрированных средств просмотра, помечайте форму как Clean и ВОЗВРАТИТ значение S_OK.  <br/> |
|Форма находится в одном из состояний Хандсофф, а параметру _пмессаже_ ЗАДАНО значение null.  <br/> |Возвращает Е_ИНВАЛИДАРГ.  <br/> |
|Форма находится в состоянии, отличном от одного из состояний Хандсофф или в режиме "каракули".  <br/> |Возвращает Е_УНЕКСПЕКТЕД.  <br/> |
   
Для получения дополнительных сведений о сохранении объектов хранилища обратитесь к документации по методам [иперсистстораже:: савекомплетед](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststorage-savecompleted) или [IPersistFile:: савекомплетед](https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersistfile-savecompleted) . 
  
## <a name="see-also"></a>См. также

- [IPersistMessage : IUnknown](ipersistmessageiunknown.md)
- [Состояния форм](form-states.md)
