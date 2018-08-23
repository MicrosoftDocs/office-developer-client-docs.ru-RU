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
ms.openlocfilehash: 30aaaaa250155215149a941da7f7e528d65b8dc3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592201"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Выполняет принудительное все сообщения, ожидающие отправку и получение для сразу же отправки или загрузки. Объект состояния очереди MAPI и объекты состояния, реализуемые поставщиками транспорта поддерживают этот метод.
  
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
  
> [in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.
    
 _cbTargetTransport_
  
> [in] Число байтов в идентификатор записи, на который указывает параметр _lpTargetTransport_ . Параметр _cbTargetTransport_ имеет значение только на вызовы объекта состояние очереди MAPI. Для вызовов поставщика транспорта параметр _cbTargetTransport_ имеет значение 0. 
    
 _lpTargetTransport_
  
> [in] Указатель на идентификатор записи поставщика транспорта, который является очистка очереди сообщений. Параметр _lpTargetTransport_ имеет значение только на вызовы объекта состояние очереди MAPI. Для вызовов для поставщика транспорта _lpTargetTransport_ параметру присвоено значение NULL. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет операцию сброса. Можно задать следующие флажки:
    
FLUSH_ASYNC_OK 
  
> Списание операция может возникнуть асинхронно. Этот флаг применяется только к объект состояния очереди MAPI. 
    
FLUSH_DOWNLOAD 
  
> Очередь входящих сообщений должны быть очищены.
    
FLUSH_FORCE 
  
> Списание операции копирования независимо от того, несмотря на возможность при снижении производительности. Этот флаг должны быть установлены при нацелено поставщика асинхронной передачи.
    
FLUSH_NO_UI 
  
> Состояние объекта не должно отображать индикатор хода выполнения.
    
FLUSH_UPLOAD 
  
> Должны быть очищены очередей исходящих сообщений.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Списание операция выполнена успешно.
    
MAPI_E_BUSY 
  
> Другой операции находится в стадии разработки; должны для выполнения или она должна быть остановлена, перед этой операции может быть инициирован.
    
MAPI_E_NO_SUPPORT 
  
> Состояние объект не поддерживает эту операцию, как указано в отсутствие флага STATUS_FLUSH_QUEUES в свойстве **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) состояние объекта.
    
## <a name="remarks"></a>Замечания

Метод **IMAPIStatus::FlushQueues** запросов, что диспетчер очереди MAPI или поставщика транспорта немедленно отправить все сообщения в очереди исходящих сообщений или получение всех сообщений из очереди входящих. **FlushQueues** реализована только путем объект состояния очереди MAPI и объекты состояния, транспорта питания поставщиков. 
  
MAPI_E_BUSY должны возвращаться для асинхронных запросов, чтобы клиенты могут продолжать работой. 
  
По умолчанию **FlushQueues** не синхронный режим; элемент управления не возвращает вызывающему до завершения очистки. Только сброса операции, выполняемой диспетчером очереди MAPI могут быть асинхронных; Клиенты запрашивают это поведение, установив флаг FLUSH_ASYNC_OK. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Реализация поставщика транспорта удаленного **FlushQueues** задает бит в свойстве **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) в строке состояния объект вход в систему для управления как очищаются очереди. Если средство просмотра удаленных передает флаг FLUSH_UPLOAD, метод **FlushQueues** следует устанавливать биты STATUS_INBOUND_ENABLED и STATUS_INBOUND_ACTIVE. Если средство просмотра удаленных передает флаг FLUSH_DOWNLOAD, метод **FlushQueues** следует устанавливать биты STATUS_OUTBOUND_ENABLED и STATUS_OUTBOUND_ACTIVE. Затем **FlushQueues** должен возвращать значение S_OK. Затем диспетчер очереди MAPI начнет соответствующие действия, отправка и загрузка сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Объект состояния очереди MAPI — это директива для переноса всех сообщений, конечные точки или из поставщика соответствующий транспортный протокол. При вызове поставщика транспорта отдельных состояние объекта, они управляются только сообщения для этого поставщика.
  
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[Каноническое свойство PidTagStatusCode](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

