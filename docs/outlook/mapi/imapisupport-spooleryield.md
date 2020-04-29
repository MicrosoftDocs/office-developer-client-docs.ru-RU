---
title: имаписуппортспулериелд
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerYield
api_type:
- COM
ms.assetid: f5c6ba8f-4ef5-4d60-b4e6-5b9160ec4e99
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f6cdebf82d8b84ada3d029865867c5192af90b0d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409911"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет управление ЦП диспетчеру очереди MAPI, чтобы он мог выполнять любые задачи, которые он считает необходимым.
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> Резервирования должно быть равно нулю.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Поставщик транспорта успешно освободил ЦП.
    
MAPI_W_CANCEL_MESSAGE 
  
> Предписывает поставщику транспорта прекратить доставку сообщения всем получателям, которые еще не получили его.
    
## <a name="remarks"></a>Примечания

Метод **имаписуппорт:: спулериелд** реализован для объектов поддержки поставщика транспорта. Поставщики транспорта вызывают **спулериелд** , чтобы разрешить диспетчеру очереди MAPI выполнить необходимую обработку. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызывайте **спулериелд** при выполнении длительных операций, которые можно приостановить. Это позволяет приложениям переднего плана выполняться во время длительной операции, например при доставке большого списка получателей в занятой сети. 
  
Если **спулериелд** возвращается с MAPI_W_CANCEL_MESSAGE, диспетчер очереди MAPI обнаружил, что сообщение больше не должно отправляться. Возвращайте MAPI_E_USER_CANCEL в вызывающий процесс и выйдите из него, если это возможно. 
  
Для получения дополнительных сведений о возможностях диспетчера очереди MAPI обратитесь к разделу [взаимодействие с диспетчером очереди MAPI](interacting-with-the-mapi-spooler.md).
  
## <a name="see-also"></a>См. также



[IMAPISupport: IUnknown](imapisupportiunknown.md)

