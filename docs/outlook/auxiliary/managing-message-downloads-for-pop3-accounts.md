---
title: Управление скачиванием сообщений для учетных записей POP3
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b4218aa6-1591-49db-9782-f286135fc79a
description: В этом разделе описывается, как поставщик POP3 Outlook использует историю уникального описания (UIDL) в учетной записи POP3 для идентификации сообщений, загруженных или удаленных поставщиком с сервера POP3, чтобы избежать скачивания одного и того же сообщения несколько раз.
ms.openlocfilehash: 35c50d83c317ebefa52fd9bfcb348c8411a06f25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322248"
---
# <a name="managing-message-downloads-for-pop3-accounts"></a>Управление скачиванием сообщений для учетных записей POP3

В этом разделе описывается, как поставщик POP3 Outlook использует историю уникального описания (UIDL) в учетной записи POP3 для идентификации сообщений, загруженных или удаленных поставщиком с сервера POP3, чтобы избежать скачивания одного и того же сообщения несколько раз.
  
## <a name="introduction-to-pop"></a>Введение в POP

Протокол POP указывает протокол уровня приложения для почтового клиента, например Outlook, для скачивания сообщений электронной почты с почтового сервера. Она позволяет пользователю скачать копию сообщения электронной почты на локальное устройство (например, смартфон или компьютер), а также оставить копию на сервере или удалить ее. Протокол поддерживает только один почтовый клиент, который должен быть подключен к почтовому ящику одновременно. Он определяет только способ извлечения сообщений электронной почты с почтового сервера, но не их отправки. При использовании POP почтовый клиент обычно должен проверять новые сообщения электронной почты, подключаться к почтовому серверу только в течение времени, необходимого для загрузки новых сообщений, и не оставаться на связи с сервером для получения новых уведомлений о почте. POP поддерживает только сообщения электронной почты, но не другие типы элементов, такие как контакты и встречи, если они не инкапсулированы в сообщение электронной почты. ПРОТОКОЛ POP3 имеет версию 3.
  
Сообщения для учетной записи POP идентифицируются уникальными идентификаторами (UID). Почтовый клиент, который оставляет почту на сервере, использует команду UIDL для получения карты UIDL, которая связывает каждое сообщение, доставленное в почтовый ящик, с его UID. Клиент также получает историю UIDL для сообщений, которые были загружены или удалены для почтового ящика на этом клиенте. На основе истории UIDL клиент может определить, какие сообщения являются новыми и должны быть загружены.

- Поиск истории скачивания сообщений для учетной записи [POP3:](locating-the-message-download-history-for-a-pop3-account.md)в этом разделе описывается, как почтовый клиент получает доступ к свойству [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) для получения истории UIDL для сообщений в клиентской учетной записи "Входящие" учетной записи POP3. 
    
- [Parsing the message download history for a POP3 account](parsing-the-message-download-history-for-a-pop3-account.md): This topic describes how to parse the POP3 BLOB that represents the UIDL history for messages in the client Inbox of a POP3 account, to identify the messages that have been downloaded or deleted on that account.
    
## <a name="see-also"></a>См. также

- [Управление учетными записями Outlook](outlook-account-management.md)    
- [Поиск журнала скачивания сообщений для учетной записи POP3](locating-the-message-download-history-for-a-pop3-account.md) 
- [Анализ журнала скачивания сообщений для учетной записи POP3](parsing-the-message-download-history-for-a-pop3-account.md)   
- [PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md)  
- [Constants (Account management API)](constants-account-management-api.md)    
- [Свойства (API управления учетной записью)](properties-account-management-api.md)
    

