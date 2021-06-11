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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Заставляет все сообщения, ожидаемые для отправки или отправки, немедленно загружаться или загружаться. Объекты состояния спулера MAPI и объекты состояния, реализуемые поставщиками транспорта, поддерживают этот метод.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом.
    
 _cbTargetTransport_
  
> [in] Количество byte в идентификаторе входа, на который указывает параметр _lpTargetTransport._ Параметр  _cbTargetTransport_ задан только для звонков к объекту состояния spooler MAPI. Для вызовов к поставщику транспорта параметр  _cbTargetTransport_ задан в 0. 
    
 _lpTargetTransport_
  
> [in] Указатель на идентификатор входа поставщика транспорта, который должен смывать очереди сообщений. Параметр  _lpTargetTransport_ задан только для звонков к объекту состояния spooler MAPI. Для вызовов к поставщику транспорта параметр  _lpTargetTransport_ задан в NULL. 
    
 _ulFlags_
  
> [in] Битмаска флагов, контролируемая операцией флеша. Можно установить следующие флаги:
    
FLUSH_ASYNC_OK 
  
> Операция флеша может происходить асинхронно. Этот флаг применяется только к объекту состояния пульпера MAPI. 
    
FLUSH_DOWNLOAD 
  
> Очереди входящих сообщений должны быть смыть.
    
FLUSH_FORCE 
  
> Операция флеша должна происходить независимо, несмотря на вероятность снижения производительности. Этот флаг должен быть установлен, когда асинхронный поставщик транспорта является целевым.
    
FLUSH_NO_UI 
  
> Объект состояния не должен отображать индикатор прогресса.
    
FLUSH_UPLOAD 
  
> Исходяющие очереди сообщений должны быть смыть.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция флеша прошла успешно.
    
MAPI_E_BUSY 
  
> В настоящее время продолжается другая операция; ее следует разрешить завершить или остановить до начала этой операции.
    
MAPI_E_NO_SUPPORT 
  
> Объект состояния не поддерживает эту операцию, о чем свидетельствует отсутствие флага STATUS_FLUSH_QUEUES в  свойстве PR_RESOURCE_METHODS объекта состояния[(PidTagResourceMethods).](pidtagresourcemethods-canonical-property.md)
    
## <a name="remarks"></a>Примечания

Метод **IMAPIStatus::FlushQueues** запрашивает, чтобы шпалер MAPI или поставщик транспорта немедленно отправили все сообщения в исходящую очередь или получили все сообщения из входящих очередей. **FlushQueues** реализуется только объектом состояния spooler MAPI и объектами состояния, которые поставляют поставщики транспорта. 
  
MAPI_E_BUSY должны быть возвращены для асинхронных запросов, чтобы клиенты могли продолжить работу. 
  
По умолчанию **FlushQueues** — это синхронная операция; управление не возвращается вызываемой, пока флеш не завершится. Асинхронной может быть только операция флеш-очистки, выполняемая шпалером MAPI; клиенты запрашивают такое поведение, FLUSH_ASYNC_OK флаг. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Реализация службой удаленного транспортного поставщика **flushQueues** задает биты в **свойстве PR_STATUS_CODE** [(PidTagStatusCode)](pidtagstatuscode-canonical-property.md)в строке состояния объекта logon, чтобы контролировать очистку очередей. Если удаленный зритель проходит в флаге FLUSH_UPLOAD, метод **FlushQueues** должен STATUS_INBOUND_ENABLED и STATUS_INBOUND_ACTIVE биты. Если удаленный зритель проходит в флаге FLUSH_DOWNLOAD, метод **FlushQueues** должен STATUS_OUTBOUND_ENABLED и STATUS_OUTBOUND_ACTIVE биты. **После этого flushQueues** должны S_OK. Затем шпалер MAPI инициирует соответствующие действия для загрузки и загрузки сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов на объект состояния spooler MAPI — это директива для передачи всех сообщений соответствующему поставщику транспорта или от него. При вызове объекта состояния отдельного поставщика транспорта затронуты только сообщения этого поставщика.
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[Каноническое свойство PidTagStatusCode](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

