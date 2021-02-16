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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Запрашивает у поставщика транспорта немедленно доставить все ожидающих входящие или исходящие сообщения.
  
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
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpTargetTransport_
  
> [in] Зарезервировано; должно быть NULL.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет очисткой очереди сообщений. Можно установить следующие флаги:
    
FLUSH_DOWNLOAD 
  
> Необходимо очистить очередь или очереди входящие сообщения.
    
FLUSH_FORCE 
  
> По возможности поставщик транспорта должен обработать этот запрос, даже если это отнимает много времени. 
    
FLUSH_NO_UI 
  
> Поставщик транспорта не должен отображать пользовательский интерфейс.
    
FLUSH_UPLOAD 
  
> Необходимо очистить очередь или очереди исходящие сообщения.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Пулер MAPI вызывает метод **IXPLogon::FlushQueues,** чтобы сообщить поставщику транспорта о том, что пулер MAPI должен начать обработку сообщений. Поставщик транспорта должен вызвать метод [IMAPISupport::ModifyStatusRow,](imapisupport-modifystatusrow.md) чтобы установить соответствующий бит для его состояния в свойстве **PR_STATUS_CODE** ([PidTagStatusCode)](pidtagstatuscode-canonical-property.md)строки состояния. После обновления строки состояния поставщик транспорта должен вернуть S_OK для вызова **FlushQueues.** Затем пулер MAPI начинает отправлять сообщения, а операция синхронна для пула MAPI. 
  
Для поддержки реализации метода [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) пулер MAPI вызывает **IXPLogon::FlushQueues** для всех объектов для запуска активных поставщиков транспорта, работающих в сеансе профиля. При вызове метода **FlushQueues** поставщика транспорта в результате вызова **IMAPIStatus::FlushQueues** клиентом обработка сообщений происходит асинхронно.
  
## <a name="see-also"></a>См. также



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

