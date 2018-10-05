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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384068"
---
# <a name="ipersistmessagehandsoffmessage"></a>IPersistMessage::HandsOffMessage

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Приводит к освобождение сообщения, его текущей формы.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Параметры

None
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщение было успешно отправлено.
    
## <a name="remarks"></a>Замечания

Перенос форм в двух HandsOff состояниях:
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
При открытии формы в одном из следующих состояний, находится в процессе хранением без возможности восстановления. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Когда форма просмотра вызывает метод **IPersistMessage::HandsOffMessage** , пока форма находится в состоянии [Normal](normal-state.md) или [NoScribble](noscribble-state.md) , рекурсивно вызова **HandsOffMessage** для каждого сообщения, внедренной в текущего сообщения и [ IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) метод для каждого объекта OLE, внедренные в текущем сообщении. Затем release текущего сообщения и всех внедренных сообщений и объекты OLE. Если форма была в обычном состоянии переход в состояние HandsOffFromNormal. Если форма была в состоянии NoScribble переход в состояние HandsOffAfterSave. После успешного перехода вызовите метод [функции IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) сообщение и возвращает значение S_OK. 
  
Когда форма просмотра вызывает **HandsOffMessage** при формы в одном из состояний HandsOff, возвратите значение E_UNEXPECTED. 
  
Дополнительные сведения о состояниях формы можно [Состояния формы](form-states.md). Дополнительные сведения о работе с состоянием HandsOff объектов хранилища [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) см. 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Состояния форм](form-states.md)

