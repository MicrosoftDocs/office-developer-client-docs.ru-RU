---
title: Модель отправки сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 653a9df6ec414aa18c44d8035a59f021d7cc19b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810031"
---
# <a name="message-submission-model"></a>Модель отправки сообщений

  
  
**Относится к**: Outlook 
  
Передача сообщений выполняется путем последовательности вызовов из очереди MAPI для поставщика транспорта. Вызовы упорядочены следующим образом:
  
1. Диспетчер очереди MAPI вызывает [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), передав в [IMessage: IMAPIProp](imessageimapiprop.md) экземпляр, чтобы начать процесс. 
    
2. Поставщика транспорта затем помещает значение ссылки — определенный идентификатор транспорта используется в следующих ссылок на это сообщение, в расположении, на который ссылается **SubmitMessage**.
    
3. Поставщика транспорта получает доступ к данным сообщений с помощью переданный экземпляры **IMessage** . Для каждого получателя в переданных **IMessage** , для которого он принимает ответственность за поставщика транспорта устанавливает для свойства **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) и затем возвращает.
    
4. Чтобы указать, если он распознает получателей, которые невозможно доставить или для создания отчетов о доставке standard, поставщика транспорта можно использовать метод [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) . **StatusRecips** является удобство для поставщиков транспорта, которые определено, что некоторые из получателей невозможно доставить или от их базовой системы обмена сообщениями, который может пользователя или клиентских приложений, который был получен сведений о доставке оказаться полезными. 
    
5. Диспетчер очереди MAPI вызов [IXPLogon::EndMessage](ixplogon-endmessage.md) отключен окончательный ответственности наличии-сообщения из очереди MAPI для поставщика транспорта. 
    
6. Диспетчер очереди MAPI можно использовать [IXPLogon::TransportNotify](ixplogon-transportnotify.md) для отмены обработки при выполнении вызова **SubmitMessage** или **EndMessage** сообщения. 
    

