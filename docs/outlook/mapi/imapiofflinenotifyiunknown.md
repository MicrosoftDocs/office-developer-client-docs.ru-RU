---
title: IMAPIOfflineNotify IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: adcb8e78d4e85e19d4102795aa4d43f06a7f86ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568149"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отправка уведомлений обратных вызовов в клиент поддерживает Microsoft Outlook 2010 и Microsoft Outlook 2013.
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[Уведомления](imapiofflinenotify-notify.md) <br/> |Отправляет уведомления об изменениях в состоянии подключения к клиенту.  <br/> |
   
## <a name="remarks"></a>Примечания

Клиент должен реализовывать этот интерфейс и передать указатель на него в качестве члена группы в **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** при настройке обратных вызовов с помощью **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Следовательно Outlook 2010 или Outlook 2013 могут использовать этот интерфейс для отправки уведомлений обратных вызовов для клиента. 
  
## <a name="see-also"></a>См. также



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Об API автономного режима](about-the-offline-state-api.md)
  
[Константы MAPI](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

