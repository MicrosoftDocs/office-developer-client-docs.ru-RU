---
title: IMAPISupportSpoolerYield
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
ms.openlocfilehash: d90f502e2cd7f97ac273ebecedbd0363097b1d60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584956"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Передает управление процессора диспетчер очереди MAPI, чтобы он может выполнять любые задачи рассматриваются необходимые.
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> Зарезервировано; должно быть равно нулю.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Поставщика транспорта успешно выпущен ЦП.
    
MAPI_W_CANCEL_MESSAGE 
  
> Указывает, что поставщик транспорта для остановки доставки сообщения получателям, которые еще не получена.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::SpoolerYield** реализуется для объектов поддержки поставщика транспорта. Поставщики транспорта вызовите **SpoolerYield** , чтобы разрешить диспетчер очереди MAPI для выполнения все необходимые действия. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов **SpoolerYield** при выполнении длительных операций, которые могут быть приостановлено. Это позволяет приложениям переднего плана для запуска во время длительной операции, такие как доставки для большого количества получателей в сети «занят». 
  
Если **SpoolerYield** возвращает с MAPI_W_CANCEL_MESSAGE, диспетчер очереди MAPI определяет, что сообщение больше не было отправлено. Снова MAPI_E_USER_CANCEL вызывающего процесса и exit, если это возможно. 
  
Дополнительные сведения о выдаче диспетчер очереди MAPI см [Диспетчер очереди MAPI](interacting-with-the-mapi-spooler.md).
  
## <a name="see-also"></a>См. также



[IMAPISupport: IUnknown](imapisupportiunknown.md)

