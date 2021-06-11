---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 84f0ca88403980ff9ea1c91821a8a3d7edae74fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309718"
---
# <a name="ipersistmessagehandsoffmessage"></a>IPersistMessage::HandsOffMessage

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вызывает выпуск текущего сообщения формы.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщение было успешно выпущено.
    
## <a name="remarks"></a>Примечания

Формы переходят в два состояния handsOff:
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Когда форма находится в любом из этих штатов, она находится в процессе хранения на постоянной основе. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если зритель формы вызывает **метод IPersistMessage::HandsOffMessage,** пока ваша форма находится в состоянии [Normal](normal-state.md) или [NoScribble,](noscribble-state.md) повторно вызывайте **HandsOffMessage** для каждого сообщения, встроенного в текущее сообщение, и метод [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) для каждого объекта OLE, встроенного в текущее сообщение. Затем отпустите текущее сообщение и все встроенные сообщения и объекты OLE. Если форма была в нормальном состоянии, переходите в состояние HandsOffFromNormal. Если форма была в состоянии NoScribble, переходите в состояние HandsOffAfterSave. После успешного перехода позвоните в [метод IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) и S_OK. 
  
Когда зритель форм вызывает **HandsOffMessage,** пока ваша форма находится в любом из состояниях HandsOff, E_UNEXPECTED. 
  
Дополнительные сведения о различных состояниях формы см. в дополнительных [сведениях о состояниях форм.](form-states.md) Дополнительные сведения о работе с состоянием handsOff объектов хранения см. в методе [IPersistStorage::HandsOffStorage.](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Состояния форм](form-states.md)

