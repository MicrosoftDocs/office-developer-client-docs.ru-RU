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
ms.openlocfilehash: 940cf0cf377f1b38071df5e3c300ccb7d685e5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439879"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поддерживает Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013 при отправке клиенту отзовов уведомлений.
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[Уведомить](imapiofflinenotify-notify.md) <br/> |Отправляет клиенту уведомления об изменениях в состоянии подключения.  <br/> |
   
## <a name="remarks"></a>Примечания

Клиент должен реализовать этот интерфейс и передать ему указатель в качестве участника в MAPIOFFLINE_ADVISEINFO при **[настройке](mapioffline_adviseinfo.md)** вызовов с помощью **[IMAPIOfflineMgr:::Advise](imapiofflinemgr-advise.md)**. Впоследствии Outlook 2010 или Outlook 2013 г. сможет использовать этот интерфейс для отправки клиенту отзова уведомлений. 
  
## <a name="see-also"></a>См. также



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Об API автономного режима](about-the-offline-state-api.md)
  
[��������� MAPI](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

