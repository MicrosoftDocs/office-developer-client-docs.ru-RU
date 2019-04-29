---
title: Сведения об API управления учетными записями
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'API управления учетными записями предоставляет доступ к сведениям учетной записи и поддерживает уведомления об изменениях в учетной записи. Как клиенты этого API, поставщики почты выполняют следующие действия:'
ms.openlocfilehash: 76520b7cc7f28ede28257729e4e4fbe2d5096290
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426251"
---
# <a name="about-the-account-management-api"></a>Сведения об API управления учетными записями

API управления учетными записями предоставляет доступ к сведениям учетной записи и поддерживает уведомления об изменениях в учетной записи. Как клиенты этого API, поставщики почты выполняют следующие действия:
  
1. Используйте [иолкаккаунтманажер](iolkaccountmanager.md) для управления доступом к учетным записям и настройки уведомлений об изменениях учетной записи. 
    
2. Реализация и использование [иолкаккаунтнотифи](iolkaccountnotify.md) для отправки уведомлений об изменениях учетной записи. 
    
3. Используйте [иолкенум](iolkenum.md) для перечисления учетных записей. 
    
4. Используйте [иолкаккаунт](iolkaccount.md) для получения и задания свойств и других сведений об учетной записи. Клиенты получают этот интерфейс с помощью [иолкаккаунтманажер:: финдаккаунт](iolkaccountmanager-findaccount.md) или [Иолкенум:: GetNext](iolkenum-getnext.md) для доступа к отдельной учетной записи. 
    
5. Реализуйте и используйте [иолкаккаунселпер](iolkaccounthelper.md) для предоставления вспомогательных функций диспетчера учетных записей, включая извлечение имени профиля учетной записи и текущего сеанса MAPI. 
    
6. Реализуйте и используйте [иолкеррорункновн](iolkerrorunknown.md) , чтобы предоставить дополнительные сведения об ошибке в **иолкаккаунтманажер**, **иолкаккаунтнотифи**и **иолкаккаунт**. 

##  <a name="account-management-api-components"></a>Компоненты API управления учетными записями

API управления учетными записями предоставляет следующие определения, типы данных, интерфейсы, именованные свойства и свойства.
  
### <a name="definitions"></a>Определения
  
- [Constants (Account management API)](constants-account-management-api.md)
    
### <a name="data-types"></a>Типы данных
  
- [ACCT_BIN](acct_bin.md)
    
- [ACCT_VARIANT](acct_variant.md)
    
### <a name="interfaces"></a>Интерфейсы
  
- [IOlkAccount](iolkaccount.md)
    
- [IOlkAccountHelper](iolkaccounthelper.md)
    
- [IOlkAccountManager](iolkaccountmanager.md)
    
- [IOlkAccountNotify](iolkaccountnotify.md)
    
- [IOlkEnum](iolkenum.md)
    
- [IOlkErrorUnknown](iolkerrorunknown.md)
    
### <a name="named-properties"></a>Именованные свойства
  
- [PidLidInternetAccountName](pidlidinternetaccountname.md)
    
- [PidLidInternetAccountStamp](pidlidinternetaccountstamp.md)
    
### <a name="properties"></a>Свойства
  
- [PidTagNextSendAcct](pidtagnextsendacct.md)
    
- [PidTagPrimarySendAccount](pidtagprimarysendaccount.md)
    
- [PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md)
    
- [PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md)
    
- [PROP_ACCT_ID](prop_acct_id.md)
    
- [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md)
    
- [PROP_ACCT_NAME](prop_acct_name.md)
    
- [PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md)
    
- [PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md)
    
- [PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md)
    
- [PROP_ACCT_STAMP](prop_acct_stamp.md)
    
- [PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)
    
- [PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md)
    
- [PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md)
    
- [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md)
    
- [PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md)
    

