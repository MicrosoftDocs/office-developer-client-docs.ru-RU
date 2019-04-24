---
title: IOlkAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b7cb295-fc77-a8b9-aac9-e548f3b4afcb
ms.openlocfilehash: 007a44d13565889b4775f2d3fe9979685e1878b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322276"
---
# <a name="iolkaccount"></a>IOlkAccount

Поддержка получения и установки свойств и других сведений об учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследование от:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
|Предоставлено:  <br/> |[Иолкаккаунтманажер:: финдаккаунт](iolkaccountmanager-findaccount.md) и [Иолкенум:: GetNext](iolkenum-getnext.md) <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_иолкаккаунт  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
|[Жетаккаунтинфо](iolkaccount-getaccountinfo.md) <br/> |Получает тип и категории указанной учетной записи.  <br/> |
|[Предл](iolkaccount-getprop.md) <br/> |Получает значение свойства указанной учетной записи. В приведенной ниже таблице свойств.  <br/> |
|[Сетпроп](iolkaccount-setprop.md) <br/> |Задает значение указанного свойства учетной записи. В приведенной ниже таблице свойств.  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
|[Фримемори](iolkaccount-freememory.md) <br/> |Освобождает память, выделенную интерфейсом **иолкаккаунт** .  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
|[SaveChanges](iolkaccount-savechanges.md) <br/> |Фиксирует изменения объекта Account, записывая в хранилище реестра.  <br/> |
   
## <a name="properties"></a>Свойства

|||
|:-----|:-----|
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Представляет идентификатор папки доставки по умолчанию для учетной записи.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Представляет идентификатор элемента хранилища доставки по умолчанию для учетной записи.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Возвращает идентификатор учетной записи в Outlook 2000 и более ранних версиях Outlook.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |Значение true, если учетная запись является учетной записью Microsoft Exchange.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Возвращает идентификатор учетной записи в версиях Outlook, начиная с Outlook 2002.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Возвращает имя учетной записи.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Получает уникальный идентификатор (UID) для раздела профиля, в котором хранятся параметры учетной записи.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Возвращает штамп "Отправить" для учетной записи.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Представляет идентификатор папки по умолчанию для отправленных элементов для учетной записи.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Возвращает метку учетной записи.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Возвращает отображаемое имя пользователя.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Указывает адрес электронной почты для учетной записи.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Представляет структуру [аккт_бин](acct_bin.md) , которая содержит UID учетной записи Exchange.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Возвращает или задает идентификатор записи адресной книги для учетной записи.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Представляет параметры транспорта, которые Microsoft Outlook использует для определения необходимых задач синхронизации и отключения элементов пользовательского интерфейса, которые не поддерживаются учетной записью.  <br/> |
   
## <a name="remarks"></a>Замечания

Этот интерфейс возвращается методом **иолкаккаунтманажер:: финдаккаунт** при поиске учетной записи, которая поддерживает **иолкаккаунт** и **иолкенум::-Next** при возврате следующей учетной записи в перечислителе. 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md)  
- [Constants (Account management API)](constants-account-management-api.md)

