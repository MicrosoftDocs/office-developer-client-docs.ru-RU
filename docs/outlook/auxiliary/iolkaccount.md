---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: 007a44d13565889b4775f2d3fe9979685e1878b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425066"
---
# <a name="iolkaccount"></a>IOlkAccount

Поддерживает получение и настройку свойств и другую информацию об учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
|Предоставлено:  <br/> |[IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) и [IOlkEnum::GetNext](iolkenum-getnext.md) <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IOlkAccount  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
| *Член placeholder*  <br/> | *Не поддерживается или не документируется.*  <br/> |
| *Член placeholder*  <br/> | *Не поддерживается или не документируется.*  <br/> |
| *Член placeholder*  <br/> | *Не поддерживается или не документируется.*  <br/> |
| *Член placeholder*  <br/> | *Не поддерживается или не документируется.*  <br/> |
| *Член placeholder*  <br/> | *Не поддерживается или не документируется.*  <br/> |
| *Член placeholder*  <br/> | *Не поддерживается или не документируется.*  <br/> |
|[GetAccountInfo](iolkaccount-getaccountinfo.md) <br/> |Получает тип и категории указанной учетной записи.  <br/> |
|[GetProp](iolkaccount-getprop.md) <br/> |Получает значение указанного свойства учетной записи. См. таблицу Свойства ниже.  <br/> |
|[SetProp](iolkaccount-setprop.md) <br/> |Задает значение указанного свойства учетной записи. См. таблицу Свойства ниже.  <br/> |
| *Член placeholder*  <br/> | *Не поддерживается или не документируется.*  <br/> |
| *Член placeholder*  <br/> | *Не поддерживается или не документируется.*  <br/> |
| *Член placeholder*  <br/> | *Не поддерживается или не документируется.*  <br/> |
|[FreeMemory](iolkaccount-freememory.md) <br/> |Освободит память, выделенную **интерфейсом IOlkAccount.**  <br/> |
| *Член placeholder*  <br/> | *Не поддерживается или не документируется.*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |Внося изменения в объект учетной записи, написав в хранилище реестра.  <br/> |
   
## <a name="properties"></a>Свойства

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Представляет ID записи папки доставки по умолчанию для учетной записи.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Представляет ID входа в хранилище доставки по умолчанию для учетной записи.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Возвращает идентификатор учетной записи в Outlook 2000 и более ранних версиях Outlook.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |True, если учетная запись является учетной записью Microsoft Exchange.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Возвращает идентификатор учетной записи в версиях Outlook с Outlook 2002 г.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Возвращает имя учетной записи.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Извлекает уникальный идентификатор (UID) для раздела профилей, который хранит предпочтения учетной записи.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Возвращает штамп "отправить" учетную запись.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Представляет ID записи папки по умолчанию для отправленных элементов для учетной записи.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Возвращает штамп учетной записи.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Возвращает имя отображения пользователя.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Указывает адрес электронной почты для учетной записи.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Представляет [структуру ACCT_BIN,](acct_bin.md) которая содержит UID учетной записи Exchange учетной записи.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Извлекает или задает ID записи адресной книги для учетной записи.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Представляет параметры транспорта, которые корпорация Майкрософт Outlook для определения необходимых задач синхронизации и отключения элементов пользовательского интерфейса (пользовательского интерфейса), которые учетная запись не поддерживает.  <br/> |
   
## <a name="remarks"></a>Примечания

Этот интерфейс возвращается **IOlkAccountManager::FindAccount** при поиске учетной записи, поддерживающего **IOlkAccount** и **IOlkEnum::GetNext** при получении следующей учетной записи в переуметоре. 
  
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md)  
- [Constants (Account management API)](constants-account-management-api.md)

