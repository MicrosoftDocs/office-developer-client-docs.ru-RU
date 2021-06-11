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
ms.openlocfilehash: f6cdebf82d8b84ada3d029865867c5192af90b0d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409911"
---
# <a name="imapisupportspooleryield"></a>IMAPISupport::SpoolerYield

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет управление ЦП пуллеру MAPI, чтобы он выполнял любые задачи, которые он считает необходимыми.
  
```cpp
HRESULT SpoolerYield(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> Зарезервировано; должно быть нулевой.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Поставщик транспорта успешно выпустил ЦП.
    
MAPI_W_CANCEL_MESSAGE 
  
> Предписывает поставщику транспорта прекратить доставку сообщения тем получателям, которые еще не получили его.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::SpoolerYield** реализован для объектов поддержки поставщиков транспорта. Поставщики транспорта **звонят в SpoolerYield,** чтобы разрешить шпалеру MAPI выполнять любую необходимую обработку. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов **SpoolerYield** при выполнении длительных операций, которые можно приостановить. Это позволяет приложениям переднего плана работать во время длительной операции, например доставку в большой список получателей через занятую сеть. 
  
Если **SpoolerYield** возвращается с MAPI_W_CANCEL_MESSAGE, пульпер MAPI решил, что сообщение больше не следует отправлять. Возвращайте MAPI_E_USER_CANCEL процесс вызова и выход, если это возможно. 
  
Дополнительные сведения о том, как уступить шпалеру MAPI, см. в ссылке [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md).
  
## <a name="see-also"></a>См. также



[IMAPISupport: IUnknown](imapisupportiunknown.md)

