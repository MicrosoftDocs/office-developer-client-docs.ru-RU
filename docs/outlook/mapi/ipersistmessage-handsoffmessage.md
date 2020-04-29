---
title: иперсистмессажехандсоффмессаже
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Заставляет форму выпустить текущее сообщение.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Параметры

Нет
  
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Сообщение успешно выпущено.
    
## <a name="remarks"></a>Примечания

Формы переходят на два состояния Хандсофф:
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Если форма находится в любом из этих состояний, она находится в процессе окончательного сохранения. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Когда средство просмотра формы вызывает метод **иперсистмессаже:: хандсоффмессаже** , когда форма находится в [обычном](normal-state.md) или [нерисованном](noscribble-state.md) состоянии, рекурсивно вызовите **хандсоффмессаже** для каждого сообщения, внедренного в текущее сообщение, и метод [иперсистстораже:: хандсоффстораже](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) для каждого объекта OLE, внедренного в текущее сообщение. Затем отпустите текущее сообщение и все внедренные сообщения и объекты OLE. Если форма находилась в нормальном состоянии, переходите в состояние HandsOffFromNormal. Если форма находилась в состоянии Scribble, переходите в состояние HandsOffAfterSave. После успешного перехода вызовите метод [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) сообщения и возвратит S_OK. 
  
Когда средство просмотра формы вызывает **хандсоффмессаже** , когда форма находится в любом из состояний хандсофф, возвращайте E_UNEXPECTED. 
  
Дополнительные сведения о различных состояниях формы можно узнать в статье [состояния форм](form-states.md). Дополнительные сведения о том, как работать с состоянием объектов хранилища Хандсофф, можно узнать в методе [иперсистстораже:: хандсоффстораже](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) . 
  
## <a name="see-also"></a>См. также



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[Состояния форм](form-states.md)

