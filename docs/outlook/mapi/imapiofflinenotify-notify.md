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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отправляет клиенту уведомления об изменениях состояния подключения.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Parameters

 _pNotifyInfo_
  
> [in] Уведомление, которое Outlook клиенту. В уведомлении указывается часть измененного состояния подключения, старое состояние подключения и новое состояние подключения.
    
## <a name="remarks"></a>Примечания

Outlook этот метод используется для отправки клиенту отзова уведомлений. Чтобы сделать этот интерфейс доступным для Microsoft Outlook 2010, русская версия или Microsoft Outlook 2013, клиент должен реализовать этот интерфейс и передать **[](mapioffline_adviseinfo.md)** ему указатель в качестве участника MAPIOFFLINE_ADVISEINFO при настройке вызовов с помощью **[IMAPIOfflineMgr:::Advise](imapiofflinemgr-advise.md)**. 
  
Клиент также передает  MAPIOFFLINE_ADVISEINFO клиентский маркер, который Outlook 2010 или Outlook 2013 г. используется в **IMAPIOfflineNotify:::Notify** для идентификации клиента, зарегистрированного для вызова уведомления. 
  
Как правило, Outlook 2010 и Outlook 2013 г. может уведомлять клиента об изменениях в режиме online/offline и других изменениях состояния подключения, но API состояния автономного подключения поддерживает только уведомления для изменений в режиме online/offline. Клиент должен игнорировать все другие уведомления.
  
## <a name="see-also"></a>См. также



[Об API автономного режима](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

