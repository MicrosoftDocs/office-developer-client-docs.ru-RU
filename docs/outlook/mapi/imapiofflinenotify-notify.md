---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 4440df4b8e4a46e13748cf47d599e16599aaf858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410695"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отправляет клиенту уведомления об изменениях в состоянии подключения.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Параметры

 _pNotifyInfo_
  
> [in] Уведомление, которое Outlook отправляет клиенту. Уведомление указывает измененную часть состояния подключения, старое состояние подключения и новое состояние подключения.
    
## <a name="remarks"></a>Примечания

Outlook использует этот метод для отправки клиенту вызовов уведомлений. Чтобы сделать этот интерфейс доступным для Microsoft Outlook 2010, русская версия или Microsoft Outlook 2013, клиент должен реализовать этот интерфейс и передать ему указатель как член в **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** при настройке вызовов с помощью **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. 
  
Клиент также передает  маркер MAPIOFFLINE_ADVISEINFO, который Outlook 2010 или Outlook 2013 использует в **IMAPIOfflineNotify::Notify** для идентификации клиента, зарегистрированного для вызова уведомления. 
  
Как правило, Outlook 2010 и Outlook 2013 могут уведомлять клиента об изменениях состояния подключения в сети или автономном режиме и других изменениях состояния подключения, но API автономного состояния поддерживает только уведомления об изменениях в сети или в автономном режиме. Клиент должен игнорировать все остальные уведомления.
  
## <a name="see-also"></a>См. также



[Об API автономного режима](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

