---
title: Получение сообщений с помощью поставщиков магазинов сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c93a4b56489c2bfb458e2e1cd872073e64d9998a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418731"
---
# <a name="receiving-messages-by-using-message-store-providers"></a>Получение сообщений с помощью поставщиков магазинов сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поставщики магазинов сообщений не должны поддерживать входящие сообщения (то есть поддерживать возможность поставщиков транспорта и пулера MAPI использовать поставщика магазина сообщений в качестве точки доставки сообщений). Однако если поставщик магазина сообщений не поддерживает входящие сообщения, его нельзя использовать в качестве магазина сообщений по умолчанию.
  
Чтобы поддерживать входящие сообщения, поставщик магазина сообщений должен сделать следующее:
  
- Поддержка [методов IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) и [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы клиентские приложения могли находить входящие сообщения. 
    
- Поддержив [метод IMsgStore::NotifyNewMail,](imsgstore-notifynewmail.md) вы можете сообщить поставщику магазина сообщений о том, что пришло новое сообщение. 
    
- Реализация уведомлений, чтобы клиенты могли зарегистрироваться для нового уведомления о сообщении. Уведомления необязательны, но поставщик должен их реализовать.
    
Последовательность вызовов метода, которая возникает при доставке входящих сообщений в хранилище сообщений, является следующим образом:
  
1. Spooler MAPI вызывает [IMsgStore::OpenEntry](imsgstore-openentry.md) с [](entryid.md) входной записью Входящие, чтобы получить [интерфейс IMAPIFolder.](imapifolderimapicontainer.md) 
    
2. Spooler MAPI вызывает [IMAPIFolder::CreateMessage,](imapifolder-createmessage.md) чтобы получить новый объект сообщения. 
    
3. Шпалер MAPI передает объект сообщения поставщику транспорта.
    
4. Поставщик транспорта заполняет свойства сообщения данными из системы обмена сообщениями и вызывает метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) объекта сообщения. 
    
5. Поставщик магазина сообщений использует метод уведомления для информирования зарегистрированных клиентов о том, что пришло новое сообщение.
    
6. Spooler MAPI вызывает метод [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) магазина сообщений. 
    
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

