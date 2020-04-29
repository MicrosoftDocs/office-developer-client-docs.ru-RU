---
title: иксплогонфлушкуеуес
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: fb26c7f366ce6a262362001773e825c60d0e4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421972"
---
# <a name="ixplogonflushqueues"></a>IXPLogon::FlushQueues

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отправляет поставщику транспорта немедленное предоставление всех ожидающих входящих и исходящих сообщений.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _улуипарам_
  
> возврата Дескриптор родительского окна всех диалоговых окон и окон, отображаемых данным методом.
    
 _кбтаржеттранспорт_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _лптаржеттранспорт_
  
> возврата Резервирования должно иметь значение NULL.
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющих, как выполняется очистка очереди сообщений. Можно задать следующие флаги:
    
FLUSH_DOWNLOAD 
  
> Очередь входящих сообщений или очереди должны быть сброшены.
    
FLUSH_FORCE 
  
> Поставщик транспорта должен обработать этот запрос, если это возможно, даже если это возможно, занимать много времени. 
    
FLUSH_NO_UI 
  
> Поставщик транспорта не должен отображать пользовательский интерфейс.
    
FLUSH_UPLOAD 
  
> Необходимо очистить очередь исходящих сообщений или очереди.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов выполнен успешно и вернул ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Диспетчер очереди MAPI вызывает метод **иксплогон:: FlushQueues** для уведомления поставщика транспорта о том, что диспетчер очереди MAPI начинает обработку сообщений. Поставщик транспорта должен вызвать метод [имаписуппорт:: модифистатусров](imapisupport-modifystatusrow.md) , чтобы задать соответствующий бит для его состояния в свойстве **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) строки состояния. После обновления строки состояния поставщик транспорта должен возвратить S_OK для вызова **FlushQueues** . После этого диспетчер очереди MAPI начинает отправку сообщений с помощью операции, которая синхронизируется с диспетчером MAPI. 
  
Для поддержки реализации метода [имапистатус:: FlushQueues](imapistatus-flushqueues.md) Диспетчер очереди MAPI вызывает **Иксплогон:: FlushQueues** для всех объектов входа для активных поставщиков транспорта, выполняемых в сеансе профиля. Когда метод **FlushQueues** поставщика транспорта вызывается в результате вызова клиентского приложения в **Имапистатус:: FlushQueues**, обработка сообщений выполняется асинхронно на клиенте.
  
## <a name="see-also"></a>См. также



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

