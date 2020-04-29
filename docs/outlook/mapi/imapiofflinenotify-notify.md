---
title: имапиоффлиненотифинотифи
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
  
Отправляет клиенту уведомления об изменениях состояния подключения.
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a>Параметры

 _пнотифинфо_
  
> возврата Уведомление, которое Outlook отправляет клиенту. Уведомление указывает часть состояния подключения, которая изменилась, старое состояние подключения и новое состояние подключения.
    
## <a name="remarks"></a>Примечания

Outlook использует этот метод для отправки обратного вызова уведомлений клиенту. Чтобы сделать этот интерфейс доступным для Microsoft Outlook 2010 или Microsoft Outlook 2013, клиент должен реализовать этот интерфейс и передать указатель на него в качестве члена в **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** при настройке обратных вызовов с помощью **[Имапиоффлинемгр:: Advise](imapiofflinemgr-advise.md)**. 
  
Клиент также передает **MAPIOFFLINE_ADVISEINFO** маркер клиента, который Outlook 2010 или Outlook 2013 использует в **Имапиоффлиненотифи:: notify** для идентификации клиента, зарегистрированного для обратного вызова уведомления. 
  
Как правило, Outlook 2010 и Outlook 2013 могут уведомлять Клиента об изменениях в Интернете или в автономном режиме, а также на других изменениях состояния подключения, но API автономного состояния поддерживает только уведомления об изменениях в Интернете и в автономном режиме. Клиент должен игнорировать все остальные уведомления.
  
## <a name="see-also"></a>См. также



[Об API автономного режима](about-the-offline-state-api.md)
  
[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)

