---
title: Свойства (Управление учетными записями API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a5204ddd-5af4-4dd8-bc83-af96ac390786
description: В этом разделе описаны свойства в API управления учетными записями.
ms.openlocfilehash: abf7422d941f581f66a118c35d2b6ff3c03e8b6b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807986"
---
# <a name="properties-account-management-api"></a>Свойства (Управление учетными записями API)

В этом разделе описаны свойства в API управления учетными записями.
  
|**Свойство**|**Описание**|
|:-----|:-----|
|[PidTagNextSendAcct](pidtagnextsendacct.md) <br/> |Это второй учетной записью «отправить» метка для сообщения.  <br/> |
|[PidTagPrimarySendAccount](pidtagprimarysendaccount.md) <br/> |Это основная учетная запись «отправить» метка для сообщения.  <br/> |
|[PROP_ACCT_DELIVERY_FOLDER](prop_acct_delivery_folder.md) <br/> |Представляет идентификатор записи папки доставки по умолчанию для учетной записи.  <br/> |
|[PROP_ACCT_DELIVERY_STORE](prop_acct_delivery_store.md) <br/> |Представляет идентификатор записи хранилища доставки по умолчанию для учетной записи.  <br/> |
|[PROP_ACCT_ID](prop_acct_id.md) <br/> |Возвращает идентификатор, который уникальным образом определяет учетную запись в профиль, в котором создается учетная запись.  <br/> |
|[PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) <br/> |Значение true, если учетная запись является учетной записью Exchange.  <br/> |
|[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) <br/> |Возвращает идентификатор учетной записи, которая является уникальным для профилей Outlook.  <br/> |
|[PROP_ACCT_NAME](prop_acct_name.md) <br/> |Возвращает или задает имя учетной записи.  <br/> |
|[PROP_ACCT_PREFERENCES_UID](prop_acct_preferences_uid.md) <br/> |Получает уникальный идентификатор (UID) для раздела профиля, в которой хранятся параметры учетной записи.  <br/> |
|[PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) <br/> |Возвращает отметку учетной записи «отправить».  <br/> |
|[PROP_ACCT_SENTITEMS_EID](prop_acct_sentitems_eid.md) <br/> |Представляет идентификатор записи папки по умолчанию для отправленных элементов для учетной записи.  <br/> |
|[PROP_ACCT_STAMP](prop_acct_stamp.md) <br/> |Возвращает штамп учетной записи.  <br/> |
|[PROP_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md) <br/> |Указывает адрес электронной почты для учетной записи.  <br/> |
|[PROP_ACCT_USER_DISPLAY_NAME](prop_acct_user_display_name.md) <br/> |Возвращает или задает отображаемое имя пользователя.  <br/> |
|[PROP_INET_PASSWORD](prop_inet_password.md) <br/> |Представляет пароль пользователя для общего почтового ящика Интернета.  <br/> |
|[PROP_INET_PORT](prop_inet_port.md) <br/> |Представляет номер порта для общего почтового ящика Интернета.  <br/> |
|[PROP_INET_SERVER](prop_inet_server.md) <br/> |Представляет имя сервера общих почтовых ящиков Интернета.  <br/> |
|[PROP_INET_SSL](prop_inet_ssl.md) <br/> |Указывает, используются ли безопасного сокетов протокол SSL для общего почтового ящика Интернета.  <br/> |
|[PROP_INET_USE_SPA](prop_inet_use_spa.md) <br/> |Указывает, следует ли использовать безопасную проверку пароля (SPA) для общего почтового ящика Интернета.  <br/> |
|[PROP_INET_USER](prop_inet_user.md) <br/> |Представляет имя пользователя для общего почтового ящика Интернета.  <br/> |
|[PROP_MAPI_EMSMDB_UID](prop_mapi_emsmdb_uid.md) <br/> |Представляет структуру [ACCT_BIN](acct_bin.md) , которая содержит уникальный идентификатор учетной записи Exchange.  <br/> |
|[PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) <br/> |Получает или задает идентификатор записи адресной книги для учетной записи.  <br/> |
|[PROP_MAPI_TRANSPORT_FLAGS](prop_mapi_transport_flags.md) <br/> |Представляет параметры транспорта, используемые Outlook для определения необходимости синхронизации задач и отключить элементы пользовательского интерфейса (UI), которые учетной записи не поддерживаются.  <br/> |
|[PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md) <br/> |Указывает, сохранение копий сообщений на сервере для учетной записи POP.  <br/> |
|[PROP_SMTP_AUTH_METHOD](prop_smtp_auth_method.md) <br/> |Указывает метод проверки подлинности для учетной записи SMTP.  <br/> |
|[PROP_SMTP_PASSWORD](prop_smtp_password.md) <br/> |Представляет собой пароль учетной записи SMTP.  <br/> |
|[PROP_SMTP_PORT](prop_smtp_port.md) <br/> |Представляет номер порта SMTP учетной записи.  <br/> |
|[PROP_SMTP_SECURE_CONNECTION](prop_smtp_secure_connection.md) <br/> |Указывает тип шифрованного подключения для учетной записи SMTP.  <br/> |
|[PROP_SMTP_SERVER](prop_smtp_server.md) <br/> |Представляет имя сервера SMTP учетной записи.  <br/> |
|[PROP_SMTP_SSL](prop_smtp_ssl.md) <br/> |Указывает, следует ли использовать протокол Secure сокетов протокол SSL для учетной записи SMTP.  <br/> |
|[PROP_SMTP_USE_AUTH](prop_smtp_use_auth.md) <br/> |Указывает, следует ли использовать проверку подлинности для учетной записи SMTP.  <br/> |
|[PROP_SMTP_USE_SPA](prop_smtp_use_spa.md) <br/> |Указывает, следует ли использовать безопасную проверку пароля (SPA) для учетной записи SMTP.  <br/> |
|[PROP_SMTP_USER](prop_smtp_user.md) <br/> |Представляет имя пользователя для учетной записи SMTP.  <br/> |
   

