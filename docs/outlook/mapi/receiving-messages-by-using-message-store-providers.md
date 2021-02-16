---
title: Получение сообщений с помощью поставщиков store сообщений
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
# <a name="receiving-messages-by-using-message-store-providers"></a>Получение сообщений с помощью поставщиков store сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Поставщики store сообщений не должны поддерживать отправку входящих сообщений (то есть поддерживают возможность поставщиков транспорта и пула MAPI использовать поставщика для хранения сообщений в качестве точки доставки сообщений). Однако если поставщик вашего магазина сообщений не поддерживает отправку входящих сообщений, его нельзя использовать в качестве хранения сообщений по умолчанию.
  
Чтобы поддерживать отправку входящих сообщений, поставщик вашего магазина сообщений должен сделать следующее:
  
- Поддержка [методов IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) и [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы клиентские приложения могли находить входящие сообщения. 
    
- [Поддержив метод IMsgStore::NotifyNewMail,](imsgstore-notifynewmail.md) вы можете сообщить поставщику хранилищ сообщений о том, что поступило новое сообщение. 
    
- Реализуют уведомления, чтобы клиенты могли регистрироваться для нового уведомления о сообщении. Уведомления необязательны, но поставщик должен их реализовать.
    
Последовательность вызовов метода, которые происходят при доставке входящих сообщений в хранилище сообщений:
  
1. Пулер MAPI вызывает [IMsgStore::OpenEntry](imsgstore-openentry.md) с inbox [EntryID](entryid.md) для получения [интерфейса IMAPIFolder.](imapifolderimapicontainer.md) 
    
2. Пулер MAPI вызывает [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) для получения нового объекта сообщения. 
    
3. Пулер MAPI передает объект сообщения поставщику транспорта.
    
4. Поставщик транспорта заполняет свойства сообщения данными из системы обмена сообщениями и вызывает метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) объекта сообщения. 
    
5. Поставщик банка сообщений использует свой метод уведомления, чтобы сообщить зарегистрированным клиентам о том, что поступило новое сообщение.
    
6. Пулер MAPI вызывает метод [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) в хранилище сообщений. 
    
## <a name="see-also"></a>См. также



[���������� ��������� ���������](message-store-features.md)

