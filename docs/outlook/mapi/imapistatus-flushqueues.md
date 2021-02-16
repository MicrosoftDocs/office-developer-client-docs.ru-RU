---
title: IMAPIStatusFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5f8396ca84192e485d33fb5a96f641361b717584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432606"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Заставляет отправлять или скачивать все сообщения, ожидающих отправки или отправки. Этот метод поддерживается объектом состояния пула MAPI и объектами состояния, которые реализуют поставщики транспорта.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window of any dialog boxes or windows that this method displays.
    
 _cbTargetTransport_
  
> [in] Количествобайтов в идентификаторе записи, на который указывает параметр _lpTargetTransport._ Параметр  _cbTargetTransport задан_ только для вызовов объекта состояния пула MAPI. Для вызовов поставщика транспорта параметр  _cbTargetTransport_ имеет 0. 
    
 _lpTargetTransport_
  
> [in] Указатель на идентификатор записи поставщика транспорта, который должен очистить очереди сообщений. Параметр  _lpTargetTransport задан_ только для вызовов объекта состояния пула MAPI. Для вызовов поставщика транспорта  _параметру lpTargetTransport_ задано nULL. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет операцией очистки. Можно установить следующие флаги:
    
FLUSH_ASYNC_OK 
  
> Операция очистки может происходить асинхронно. Этот флаг применяется только к объекту состояния пула MAPI. 
    
FLUSH_DOWNLOAD 
  
> Очереди входящих сообщений необходимо очистить.
    
FLUSH_FORCE 
  
> Операция очистки должна происходить независимо от того, может ли снижение производительности. Этот флаг должен устанавливаться, когда нацелен асинхронный поставщик транспорта.
    
FLUSH_NO_UI 
  
> В объекте состояния не должен отображаться индикатор хода выполнения.
    
FLUSH_UPLOAD 
  
> Необходимо очистить очереди исходяющих сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция очистки прошла успешно.
    
MAPI_E_BUSY 
  
> В настоящее время идет другая операция; его следует разрешить завершить или остановить, прежде чем можно будет инициацию этой операции.
    
MAPI_E_NO_SUPPORT 
  
> Объект status не поддерживает эту операцию, о чем свидетельствует отсутствие флага STATUS_FLUSH_QUEUES в свойстве **PR_RESOURCE_METHODS** объекта status ([PidTagResourceMethods).](pidtagresourcemethods-canonical-property.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPIStatus::FlushQueues** запрашивает, чтобы поставщик услуг транспорта MAPI немедленно отправил все сообщения в исходящую очередь или получил все сообщения из входящих очередей. **FlushQueues** реализуется только объектом состояния пула MAPI и объектами состояния, которые ставляют поставщики транспорта. 
  
MAPI_E_BUSY должны возвращаться для асинхронных запросов, чтобы клиенты могли продолжить работу. 
  
По умолчанию **FlushQueues** является синхронной операцией; управление не возвращается вызываемой до тех пор, пока очистка не завершится. Только операция очистки, выполняемая пулером MAPI, может быть асинхронной; клиенты запрашивают такое поведение, устанавливая FLUSH_ASYNC_OK флага. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Реализация **FlushQueues** удаленного поставщика транспорта задает биты в свойстве **PR_STATUS_CODE** ([PidTagStatusCode)](pidtagstatuscode-canonical-property.md)в строке состояния объекта для логотипа, чтобы управлять очисткой очередей. Если удаленный просмотр передает флаг FLUSH_UPLOAD, метод **FlushQueues** должен установить STATUS_INBOUND_ENABLED и STATUS_INBOUND_ACTIVE биты. Если удаленный просмотр передает флаг FLUSH_DOWNLOAD, метод **FlushQueues** должен установить STATUS_OUTBOUND_ENABLED и STATUS_OUTBOUND_ACTIVE биты. **FlushQueues** затем должен возвращать S_OK. The MAPI spooler will then initiate the appropriate actions to upload and download messages. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов объекта состояния пула MAPI — это директива для передачи всех сообщений соответствующему поставщику транспорта или от него. При вызове объекта состояния отдельного поставщика транспорта это влияет только на сообщения этого поставщика.
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[Каноническое свойство PidTagStatusCode](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

