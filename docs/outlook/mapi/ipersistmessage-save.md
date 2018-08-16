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
ms.openlocfilehash: 222d8257a802739ee8e513a0ea95a13f4b99322e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809490"
---
# <a name="ipersistmessagesave"></a>IPersistMessage::Save

  
  
**Относится к**: Outlook 
  
Сохраняет измененную форму сообщение, из которого его загрузки или создан.
  
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
  
> [in] TRUE, чтобы указать, что сообщение, на который указывает, _pMessage_ сообщение, из которого форма загрузки или создания; в противном случае — FALSE. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Форма успешно сохранен.
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IPersistMessage::Save** для сохранения оптимизированная формы в сообщении, из которого его загрузки или создан. 
  
 **Сохраните** вызывается только когда форма находится в состоянии [Normal](normal-state.md) . 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Не применить сохраненные изменения; Это вызывающий объект должен сохранить изменения. Никогда не вносить изменения свойств, относящихся к сообщению формы, за исключением во время вызова **Сохранить** . 
  
Если _fSameAsLoad_ имеет значение TRUE, можно сохранить изменения в существующее сообщение формы. Если _fSameAsLoad_ имеет значение FALSE, необходимо скопировать все свойства из исходного сообщения в сообщения, на который указывает _pMessage_ перед выполнением сохранения. Метод [IMAPIProp::CopyTo](imapiprop-copyto.md) исходного сообщения служит для копирования свойств. 
  
При копировании все свойства введите состояние [NoScribble](noscribble-state.md) . При отсутствии ошибок возвращает значение S_OK. В противном случае возвращает ошибку из неудачных действия. 
  
Если **Сохранить** вызывается, когда форма находится в любом состоянии, кроме Normal, возвратите значение E_UNEXPECTED. 
  
Дополнительные сведения о сохранении объектов хранилища документации для методов [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Состояния форм](form-states.md)
