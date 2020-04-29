---
title: Свойства (API управления учетными записями)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a5204ddd-5af4-4dd8-bc83-af96ac390786
description: В этом разделе описываются свойства в API управления учетными записями.
ms.openlocfilehash: d0b8c06716bd2f3a3bb2941e098bd9f11ab87183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416337"
---
# <a name="properties-account-management-api"></a>Свойства (API управления учетными записями)

В этом разделе описываются свойства в API управления учетными записями.
  
|**Свойство**|**Описание**|
|:-----|:-----|
|[PidTagNextSendAcct](pidtagnextsendacct.md) <br/> |Это дополнительная учетная запись "Отправить" для сообщения.  <br/> |
|[PidTagPrimarySendAccount](pidtagprimarysendaccount.md) <br/> |Это метка "Отправить" основной учетной записи сообщения.  <br/> |
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Представляет идентификатор папки доставки по умолчанию для учетной записи.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Представляет идентификатор элемента хранилища доставки по умолчанию для учетной записи.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Возвращает идентификатор, который уникальным образом определяет учетную запись в профиле, в котором создается учетная запись.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |Значение true, если учетная запись является учетной записью Exchange.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Возвращает идентификатор учетной записи, уникальный для профилей Outlook.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Возвращает или задает имя учетной записи.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Получает уникальный идентификатор (UID) для раздела профиля, в котором хранятся параметры учетной записи.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Возвращает штамп "Отправить" для учетной записи.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Представляет идентификатор папки по умолчанию для отправленных элементов для учетной записи.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Возвращает метку учетной записи.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Указывает адрес электронной почты для учетной записи.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Возвращает или задает отображаемое имя пользователя.  <br/> |
|[PROP_INET_PASSWORD](prop_inet_password.md) <br/> |Представляет пароль пользователя для общего почтового ящика в Интернете.  <br/> |
|[PROP_INET_PORT](prop_inet_port.md) <br/> |Представляет номер порта для общего почтового ящика в Интернете.  <br/> |
|[PROP_INET_SERVER](prop_inet_server.md) <br/> |Представляет имя сервера для общего почтового ящика в Интернете.  <br/> |
|[PROP_INET_SSL](prop_inet_ssl.md) <br/> |Указывает, следует ли использовать протокол SSL для общего почтового ящика в Интернете.  <br/> |
|[PROP_INET_USE_SPA](prop_inet_use_spa.md) <br/> |Указывает, следует ли использовать безопасную проверку пароля (SPA) для общего почтового ящика в Интернете.  <br/> |
|[PROP_INET_USER](prop_inet_user.md) <br/> |Представляет имя пользователя для общего почтового ящика в Интернете.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Представляет структуру [ACCT_BIN](acct_bin.md) , содержащую идентификатор учетной записи Exchange.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Возвращает или задает идентификатор записи адресной книги для учетной записи.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Представляет параметры транспорта, которые Outlook использует для определения необходимых задач синхронизации и отключения элементов пользовательского интерфейса, которые не поддерживаются учетной записью.  <br/> |
|[PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md) <br/> |Указывает, что копия сообщения на сервере остается на сервере для учетной записи POP.  <br/> |
|[PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md) <br/> |Задает способ проверки подлинности, используемый для учетной записи SMTP.  <br/> |
|[PROP_SMTP_PASSWORD](prop_smtp_password.md) <br/> |Представляет пароль учетной записи SMTP.  <br/> |
|[PROP_SMTP_PORT](prop_smtp_port.md) <br/> |Представляет номер порта учетной записи SMTP.  <br/> |
|[PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md) <br/> |Указывает тип зашифрованного подключения, используемого для учетной записи SMTP.  <br/> |
|[PROP_SMTP_SERVER](prop_smtp_server.md) <br/> |Представляет имя сервера учетной записи SMTP.  <br/> |
|[PROP_SMTP_SSL](prop_smtp_ssl.md) <br/> |Указывает, следует ли использовать протокол SSL для учетной записи SMTP.  <br/> |
|[PROP_SMTP_USE_AUTH](prop_smtp_use_auth.md) <br/> |Указывает, следует ли использовать проверку подлинности для учетной записи SMTP.  <br/> |
|[PROP_SMTP_USE_SPA](prop_smtp_use_spa.md) <br/> |Указывает, следует ли использовать безопасную проверку пароля (SPA) для учетной записи SMTP.  <br/> |
|[PROP_SMTP_USER](prop_smtp_user.md) <br/> |Представляет имя пользователя для учетной записи SMTP.  <br/> |
   

