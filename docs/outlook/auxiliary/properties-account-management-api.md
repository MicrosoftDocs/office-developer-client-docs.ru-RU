---
title: Свойства (API управления учетной записью)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a5204ddd-5af4-4dd8-bc83-af96ac390786
description: В этом разделе описываются свойства API управления учетной записью.
ms.openlocfilehash: d0b8c06716bd2f3a3bb2941e098bd9f11ab87183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416337"
---
# <a name="properties-account-management-api"></a>Свойства (API управления учетной записью)

В этом разделе описываются свойства API управления учетной записью.
  
|**Свойство**|**Описание**|
|:-----|:-----|
|[PidTagNextSendAcct](pidtagnextsendacct.md) <br/> |Это вторичная отметка "отправить" учетную запись для сообщения.  <br/> |
|[PidTagPrimarySendAccount](pidtagprimarysendaccount.md) <br/> |Это основной штамп "отправить" учетную запись для сообщения.  <br/> |
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Представляет ID записи папки доставки по умолчанию для учетной записи.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Представляет ID входа в хранилище доставки по умолчанию для учетной записи.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Возвращает идентификатор, уникальный идентификатор учетной записи в профиле, в котором создается учетная запись.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |True, если учетная запись является Exchange учетной записью.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Возвращает идентификатор учетной записи, уникальный для Outlook профилей.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Возвращает или задает имя учетной записи.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Извлекает уникальный идентификатор (UID) для раздела профилей, который хранит предпочтения учетной записи.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Возвращает штамп "отправить" учетную запись.  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Представляет ID записи папки по умолчанию для отправленных элементов для учетной записи.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Возвращает штамп учетной записи.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Указывает адрес электронной почты для учетной записи.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Возвращает или задает имя отображения пользователя.  <br/> |
|[PROP_INET_PASSWORD](prop_inet_password.md) <br/> |Представляет пароль пользователя для общего почтового ящика Интернета.  <br/> |
|[PROP_INET_PORT](prop_inet_port.md) <br/> |Представляет номер порта для общего почтового ящика Интернета.  <br/> |
|[PROP_INET_SERVER](prop_inet_server.md) <br/> |Представляет имя сервера общего почтового ящика Интернета.  <br/> |
|[PROP_INET_SSL](prop_inet_ssl.md) <br/> |Указывает, следует ли использовать безопасный слой socket (SSL) для общего почтового ящика в Интернете.  <br/> |
|[PROP_INET_USE_SPA](prop_inet_use_spa.md) <br/> |Указывает, следует ли использовать проверку подлинности безопасного пароля (SPA) для общего почтового ящика в Интернете.  <br/> |
|[PROP_INET_USER](prop_inet_user.md) <br/> |Представляет имя пользователя для общего почтового ящика Интернета.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Представляет [структуру ACCT_BIN,](acct_bin.md) которая содержит UID учетной записи Exchange учетной записи.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Извлекает или задает ID записи адресной книги для учетной записи.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Представляет параметры транспорта, Outlook для определения необходимых задач синхронизации и отключения элементов пользовательского интерфейса (пользовательского интерфейса), которые учетная запись не поддерживает.  <br/> |
|[PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md) <br/> |Указывает оставить копию сообщения на сервере для учетной записи POP.  <br/> |
|[PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md) <br/> |Указывает метод проверки подлинности для учетной записи SMTP.  <br/> |
|[PROP_SMTP_PASSWORD](prop_smtp_password.md) <br/> |Представляет пароль учетной записи SMTP.  <br/> |
|[PROP_SMTP_PORT](prop_smtp_port.md) <br/> |Представляет номер порта учетной записи SMTP.  <br/> |
|[PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md) <br/> |Указывает тип зашифрованного подключения для учетной записи SMTP.  <br/> |
|[PROP_SMTP_SERVER](prop_smtp_server.md) <br/> |Представляет имя сервера учетной записи SMTP.  <br/> |
|[PROP_SMTP_SSL](prop_smtp_ssl.md) <br/> |Указывает, следует ли использовать протокол Secure Socket Layer (SSL) для учетной записи SMTP.  <br/> |
|[PROP_SMTP_USE_AUTH](prop_smtp_use_auth.md) <br/> |Указывает, следует ли использовать проверку подлинности для учетной записи SMTP.  <br/> |
|[PROP_SMTP_USE_SPA](prop_smtp_use_spa.md) <br/> |Указывает, следует ли использовать проверку подлинности безопасного пароля (SPA) для учетной записи SMTP.  <br/> |
|[PROP_SMTP_USER](prop_smtp_user.md) <br/> |Представляет имя пользователя для учетной записи SMTP.  <br/> |
   

