---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: dc802d8fef0d90672428c8bfa3662a2734637d05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807822"
---
# <a name="iolkaccount"></a>IOlkAccount

Поддерживает получение и задание свойств и другие сведения об учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Реализованный:  <br/> |Outlook  <br/> |
|Предоставлено:  <br/> |[IOlkAccountManager::FindAccount](iolkaccountmanager-findaccount.md) и [IOlkEnum::GetNext](iolkenum-getnext.md) <br/> |
|Вызывается:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IOlkAccount  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
|[GetAccountInfo](iolkaccount-getaccountinfo.md) <br/> |Получает тип и категорий для указанной учетной записи.  <br/> |
|[Функцию](iolkaccount-getprop.md) <br/> |Получает значение свойства указанной учетной записи. В разделе свойства в таблице ниже.  <br/> |
|[SetProp](iolkaccount-setprop.md) <br/> |Задает значение свойства указанной учетной записи. В разделе свойства в таблице ниже.  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
|[Свободная память](iolkaccount-freememory.md) <br/> |Освобождает память, выделенную с помощью интерфейса **IOlkAccount** .  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |Фиксирует изменения объекта учетной записи с помощью записи реестра хранилища.  <br/> |
   
## <a name="properties"></a>Свойства

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Представляет идентификатор записи папки доставки по умолчанию для учетной записи.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Представляет идентификатор записи хранилища доставки по умолчанию для учетной записи.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Возвращает идентификатор учетной записи в Outlook 2000 и более ранних версиях Outlook.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |Значение true, если учетная запись является учетной записью Microsoft Exchange.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Возвращает идентификатор учетной записи в версиях Outlook, начиная с Outlook 2002.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Возвращает имя учетной записи.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Получает уникальный идентификатор (UID) для раздела профиля, в которой хранятся параметры учетной записи.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Возвращает отметку учетной записи «отправить».  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Представляет идентификатор записи папки по умолчанию для отправленных элементов для учетной записи.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Возвращает штамп учетной записи.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Возвращает отображаемое имя пользователя.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Указывает адрес электронной почты для учетной записи.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Представляет структуру [ACCT_BIN](acct_bin.md) , которая содержит уникальный идентификатор учетной записи Exchange.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Получает или задает идентификатор записи адресной книги для учетной записи.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Представляет параметры транспорта, которые использует Microsoft Outlook для определения необходимости синхронизации задач и отключить элементы пользовательского интерфейса (UI), которые учетной записи не поддерживаются.  <br/> |
   
## <a name="remarks"></a>Замечания

Этот интерфейс возвращается **IOlkAccountManager::FindAccount** при поиске для учетной записи, которая поддерживает **IOlkAccount** и **IOlkEnum::GetNext** при получении следующего учетной записи в перечислитель. 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)  
- [Constants (Account management API)](constants-account-management-api.md)

