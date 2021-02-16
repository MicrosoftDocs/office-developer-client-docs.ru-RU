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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
API автономного состояния поддерживает вызовы, указывающие на изменения состояния подключения пользователя в Microsoft Outlook 2013 и Microsoft Outlook 2010, русская версия, например, от подключения к Сети в Outlook 2013 или Outlook 2010 до отключения. API использует глобальный автономный объект в Outlook 2013 или Outlook 2010 для отслеживания таких изменений для данного профиля учетной записи пользователя. Уведомление — единственная поддерживаемая форма вызова. Как клиенты этого API поставщики почты, которые хотят получить уведомление о таких изменениях состояния подключения, делают следующее:
  
1. Реализуют **[IMAPIOfflineNotify.](imapiofflinenotifyiunknown.md)** 
    
2. Откройте существующий автономный объект для определенного профиля с помощью **[HrOpenOfflineObj.](hropenofflineobj.md)** 
    
3. Определите, может ли объект предоставлять интерактивные или автономные уведомления с помощью **[IMAPIOffline::GetCapabilities.](imapioffline-getcapabilities.md)** 
    
4. Зарегистрируйте объект для интерактивных или автономных уведомлений с помощью **[IMAPIOfflineMgr::Advise.](imapiofflinemgr-advise.md)** Поставщики почты теперь могут получать уведомления, отправляемые Outlook 2013 или Outlook 2010 с помощью **IMAPIOfflineNotify.** 
    
5. После завершения работы удалите регистрацию для сетевых и автономных уведомлений с помощью **[IMAPIOfflineMgr::Unadvise.](imapiofflinemgr-unadvise.md)** 
    
> [!NOTE]
> Как правило, Outlook 2013 и Outlook 2010 могут уведомлять клиента об изменениях в сети и автономном режиме, а также о других изменениях, но API автономного состояния поддерживает только уведомления об изменениях в сети или автономном режиме. Клиент должен игнорировать все остальные уведомления. Дополнительные сведения см. в подразделе **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** и **[MAPIOFFLINE_NOTIFY.](mapioffline_notify.md)** 
  
 Пример клиента, который использует API автономного состояния, см. в примере надстройки [автономного состояния.](about-the-sample-offline-state-add-in.md) Пример надстройки автономного состояния — это надстройка COM, которая использует API автономного состояния для отслеживания и изменения состояния подключения.
  
Этот API предоставляет следующие возможности:
  
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
    

