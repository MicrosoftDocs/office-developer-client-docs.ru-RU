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
  
API автономного состояния поддерживает обратные вызовы, указывающие изменения состояния подключения пользователя в Microsoft Outlook 2013 и Microsoft Outlook 2010 (например, из сети в Outlook 2013 или Outlook 2010 в автономный режим). API использует глобальный автономный объект в Outlook 2013 или Outlook 2010 для отслеживания этих изменений для определенного профиля учетной записи пользователя. Уведомление — единственная поддерживаемая форма обратного вызова. В качестве клиентов этого API поставщики почты, которые хотят получать уведомления о таких изменениях состояния подключения, выполняют следующие действия:
  
1. Реализация **[имапиоффлиненотифи](imapiofflinenotifyiunknown.md)**. 
    
2. Откройте существующий автономный объект для определенного профиля с помощью **[хропеноффлинеобж](hropenofflineobj.md)**. 
    
3. Определите, имеет ли объект возможность предоставления уведомлений в Интернете или в автономном режиме с помощью **[имапиоффлине::-Capabilities](imapioffline-getcapabilities.md)**. 
    
4. Зарегистрируйте объект для интерактивных или автономных уведомлений с помощью **[имапиоффлинемгр:: Advise](imapiofflinemgr-advise.md)**. Теперь поставщики почты могут получать уведомления, которые Outlook 2013 или Outlook 2010 отправляет с помощью **имапиоффлиненотифи**. 
    
5. При завершении работы удалите регистрацию для уведомлений в Интернете и в автономном режиме с помощью **[имапиоффлинемгр:: unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> Как правило, Outlook 2013 и Outlook 2010 могут уведомлять Клиента об изменениях в Интернете или в автономном режиме, а также других изменениях, но API автономного состояния поддерживает только уведомления об изменениях в Интернете и в автономном режиме. Клиент должен игнорировать все остальные уведомления. Дополнительные сведения см. в статье **[имапиоффлиненотифи:: notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Пример клиента, использующего API автономного состояния, представлен в статье [Пример надстройки с автономным состоянием](about-the-sample-offline-state-add-in.md). Надстройка "автономное состояние" — это надстройка COM, использующая API автономного состояния для отслеживания и изменения состояния подключения.
  
Этот API предоставляет следующие функции:
  
Определения
  
- [��������� MAPI](mapi-constants.md)
    
Типы данных:
  
- **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**
    
- **[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**
    
- **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**
    
Обязанностей
  
- **[HrOpenOfflineObj](hropenofflineobj.md)**
    
Интерфейс
  
- **[имапиоффлине](imapiofflineiunknown.md)**
    
- **[имапиоффлинемгр](imapiofflinemgrimapioffline.md)**
    
- **[имапиоффлиненотифи](imapiofflinenotifyiunknown.md)**
    

