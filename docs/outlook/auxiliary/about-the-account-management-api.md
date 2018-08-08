---
title: Сведения об API управления учетными записями
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: eb6b921d-ecf8-3ce5-87ba-ac1632416b05
description: 'API управления учетными записями предоставляет доступ к сведениям учетной записи и поддерживает уведомления об изменениях учетной записи. Как клиенты этот интерфейс API поставщики почты выполните следующее:'
ms.openlocfilehash: 678143def25395c47f1c17cc99dcdcd1fb145e1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807674"
---
# <a name="about-the-account-management-api"></a>Сведения об API управления учетными записями

API управления учетными записями предоставляет доступ к сведениям учетной записи и поддерживает уведомления об изменениях учетной записи. Как клиенты этот интерфейс API поставщики почты выполните следующее:
  
1. Используйте [IOlkAccountManager](iolkaccountmanager.md) для управления доступом к учетным записям и настройка уведомлений о изменения учетной записи. 
    
2. Внедрение и использовать [IOlkAccountNotify](iolkaccountnotify.md) для отправки уведомлений о изменения учетной записи. 
    
3. Используйте [IOlkEnum](iolkenum.md) для перечисления учетных записей. 
    
4. Используйте [IOlkAccount](iolkaccount.md) для получения и задания свойств и другие сведения об учетной записи. Клиенты получить этот интерфейс через [IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) или [IOlkEnum::GetNext](iolkenum-getnext.md) для доступа к отдельным учетной записи. 
    
5. Реализация и использование [IOlkAccountHelper](iolkaccounthelper.md) для предоставления учетной записи диспетчера вспомогательных функциональных возможностей, включая начало имя профиля учетной записи и текущего сеанса MAPI. 
    
6. Реализация и использование [IOlkErrorUnknown](iolkerrorunknown.md) для предоставления дополнительных сведений об ошибке в **IOlkAccountManager**, **IOlkAccountNotify**и **IOlkAccount**. 

##  <a name="account-management-api-components"></a>Компоненты управления API учетной записи

API управления учетными записями предоставляет следующие определения, типы данных, интерфейсы, с именем свойства и свойства.
  
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
    

