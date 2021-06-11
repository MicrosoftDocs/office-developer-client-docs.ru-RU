---
title: Сведения об API автономного состояния
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410485"
---
# <a name="about-the-offline-state-api"></a>Сведения об API автономного состояния

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
API состояния автономного доступа поддерживает вызовы, указывающие на изменения состояния подключения пользователя в Microsoft Outlook 2013 и Microsoft Outlook 2010, русская версия, например, от подключения к сети в Outlook 2013 или Outlook 2010 г. до отключения. API использует глобальный автономный объект Outlook 2013 или Outlook 2010 г. для отслеживания таких изменений для данного профиля учетной записи пользователя. Уведомление — это единственная поддерживаемая форма вызова. Как клиенты этого API, поставщики почты, которые хотят получить уведомление о таких изменениях состояния подключения, делают следующее:
  
1. Реализация **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Откройте существующий автономный объект для определенного профиля с помощью **[HrOpenOfflineObj.](hropenofflineobj.md)** 
    
3. Определите, имеет ли объект возможность предоставления уведомлений в Интернете или автономном режиме с помощью **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. 
    
4. Регистрация объекта для уведомлений в интернете или автономном режиме с помощью **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Теперь поставщики почты могут получать уведомления, Outlook 2013 или Outlook 2010 г. с помощью **IMAPIOfflineNotify.** 
    
5. При остановке удалите регистрацию для уведомлений в интернете и автономном режиме с помощью **[IMAPIOfflineMgr::Unadvise.](imapiofflinemgr-unadvise.md)** 
    
> [!NOTE]
> Как правило, Outlook 2013 и Outlook 2010 г. может уведомлять клиента об изменениях в режиме online/offline, а также о других изменениях, но API состояния автономного доступа поддерживает только уведомления об изменениях в режиме online/offline. Клиент должен игнорировать все другие уведомления. Дополнительные сведения см. **[в iMAPIOfflineNotify:::Notify](imapiofflinenotify-notify.md)** и **[MAPIOFFLINE_NOTIFY.](mapioffline_notify.md)** 
  
 Пример клиента, использующего API состояния автономного доступа, см. в примере надстройки состояния в автономном [режиме.](about-the-sample-offline-state-add-in.md) Пример надстройки состояния в автономном режиме — это надстройка COM, которая использует API состояния автономного доступа для мониторинга и изменения состояния подключения.
  
В этом API содержится следующее:
  
Определения
  
- [��������� MAPI](mapi-constants.md)
    
Типы данных:
  
- **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**
    
- **[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**
    
- **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**
    
Функции:
  
- **[HrOpenOfflineObj](hropenofflineobj.md)**
    
Интерфейсы:
  
- **[IMAPIOffline](imapiofflineiunknown.md)**
    
- **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**
    
- **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**
    

