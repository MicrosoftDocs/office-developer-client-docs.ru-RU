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
ms.openlocfilehash: 54843339c6843e075ec769da5751ae2fe753f302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809021"
---
# <a name="imapiofflinenotifynotify"></a>IMAPIOfflineNotify::Notify

  
  
**Относится к**: Outlook 
  
Отправляет уведомления об изменениях в состоянии подключения к клиенту.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Параметры

 _pNotifyInfo_
  
> [in] Уведомление, Outlook отправляет клиенту. Это уведомление указывает часть состояние подключения, который был изменен, старый состояние подключения и новое состояние подключения.
    
## <a name="remarks"></a>Замечания

Outlook использует этот метод для отправки уведомлений обратных вызовов в клиент. Чтобы сделать этот интерфейс для Microsoft Outlook 2010 или Microsoft Outlook 2013, необходимо реализовать этот интерфейс и передать указатель на него в качестве члена в **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** при настройке обратных вызовов с помощью **[IMAPIOfflineMgr::Advise ](imapiofflinemgr-advise.md)**. 
  
Клиент также передает **MAPIOFFLINE_ADVISEINFO** маркера клиента, Outlook 2010 или Outlook 2013 с помощью в **IMAPIOfflineNotify::Notify** для идентификации клиента, зарегистрированных для обратного вызова для уведомления. 
  
В общем случае Outlook 2010 и Outlook 2013 может уведомлять клиента онлайновом/интерактивном режиме изменений и другие изменения состояния подключения, но автономного состояния API поддерживает только уведомления для онлайновом/интерактивном режиме изменения. Клиент должен игнорировать все уведомления.
  
## <a name="see-also"></a>См. также



[Сведения об API автономного состояния](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

