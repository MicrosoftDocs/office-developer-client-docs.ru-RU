---
title: IXPLogonFlushQueues
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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Запрашивает, чтобы поставщик транспорта немедленно доставлял все ожидающих входящие или исходящие сообщения.
  
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
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpTargetTransport_
  
> [in] Зарезервировано; должно быть NULL.
    
 _ulFlags_
  
> [in] Битмаска флагов, контролирующих выполнение очистки очереди сообщений. Можно установить следующие флаги:
    
FLUSH_DOWNLOAD 
  
> Очередь входящие сообщения или очереди должны быть смыть.
    
FLUSH_FORCE 
  
> Поставщик транспорта должен обрабатывать этот запрос, если это возможно, даже если это отнимает много времени. 
    
FLUSH_NO_UI 
  
> Поставщик транспорта не должен отображать пользовательский интерфейс.
    
FLUSH_UPLOAD 
  
> Очередь исходящие сообщения или очереди должны быть смыть.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Spooler MAPI вызывает **метод IXPLogon::FlushQueues,** чтобы сообщить поставщику транспорта, что spooler MAPI вот-вот начнет обработку сообщений. Поставщик транспорта должен вызвать метод [IMAPISupport::ModifyStatusRow,](imapisupport-modifystatusrow.md) чтобы установить соответствующий бит для его состояния в свойстве PR_STATUS_CODE[(PidTagStatusCode)](pidtagstatuscode-canonical-property.md)строки состояния.  После обновления строки состояния поставщик транспорта должен S_OK для вызова **FlushQueues.** Затем шпалер MAPI начинает отправлять сообщения, а операция синхронна с пулером MAPI. 
  
Чтобы поддержать реализацию метода [IMAPIStatus::FlushQueues,](imapistatus-flushqueues.md) шпалер MAPI вызывает **IXPLogon::FlushQueues** для всех объектов с логотипами для активных поставщиков транспорта, работающих в сеансе профиля. Когда метод **FlushQueues** поставщика транспорта вызван в результате вызова клиентского приложения в **IMAPIStatus::FlushQueues,** обработка сообщений происходит асинхронно для клиента.
  
## <a name="see-also"></a>См. также



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

