---
title: Сведения об API автономного состояния
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: df225a0852b09e048656e817c54ea28b0de59888
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808000"
---
# <a name="about-the-offline-state-api"></a>Сведения об API автономного состояния

  
  
**Относится к**: Outlook 
  
Автономные состояния API поддерживает обратных вызовов, указывающее, изменения в состоянии подключения пользователя в Microsoft Outlook 2013 и Microsoft Outlook 2010 — например, от которого online в Outlook 2013 или Outlook 2010 для отключения. API-Интерфейс используется объект глобального автономной в Outlook 2013 или Outlook 2010 для отслеживания таких изменений для профиля учетной записи указанного пользователя. Уведомления — это единственный поддерживаемого форм обратного вызова. Как клиенты этот интерфейс API почты поставщиков, кому требуется получать уведомления о такие изменения состояния подключения выполните следующие действия.
  
1. Реализация **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Откройте существующий объект автономной для определенного профиля, с помощью **[HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. Определяет, есть ли объект возможностью поддержки сетевым и автономным уведомлений с помощью **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. 
    
4. Регистрация объекта сетевым и автономным уведомлений с помощью **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Поставщики почты могут получать уведомления о том, что Outlook 2010 или Outlook 2013 отправить, используя **IMAPIOfflineNotify**. 
    
5. При завершении работы удалите регистрацию автономном и интерактивном режимах уведомлений с помощью **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> В общем случае Outlook 2013 и Outlook 2010 можно уведомление клиента онлайновом/интерактивном режиме изменения, а также другие изменения, но автономного состояния API поддерживает только уведомления для онлайновом/интерактивном режиме изменения. Клиент должен игнорировать все уведомления. Для получения дополнительных сведений см **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** и **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Пример клиента, использующего автономный режим состояния API видеть [о пример автономный режим состояние надстройки](about-the-sample-offline-state-add-in.md). Добавить пример состояние не в сети в является надстройки COM, которая использует автономный режим состояния API-Интерфейс для мониторинга и изменить состояние подключения.
  
Этот интерфейс API предоставляет следующие возможности:
  
Определения:
  
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
    

