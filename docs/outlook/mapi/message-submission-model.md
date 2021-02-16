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
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421125"
---
# <a name="message-submission-model"></a>Модель отправки сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отправка сообщений выполняется с помощью серии вызовов из пула MAPI к поставщику транспорта. Вызовы в порядке последовательности:
  
1. Пулер MAPI вызывает [IXPLogon::SubmitMessage,](ixplogon-submitmessage.md)передавая [экземпляр IMessage : IMAPIProp,](imessageimapiprop.md) чтобы начать процесс. 
    
2. Затем поставщик транспорта помещает значение ссылки ( определяемого транспортом идентификатора, используемого в последующих ссылках на это сообщение) в расположение, на которое ссылается **SubmitMessage.**
    
3. Поставщик транспорта имеет доступ к данным сообщения с помощью переданного экземпляра **IMessage.** Для каждого получателя в переданной **службе IMessage,** за которую он принимает ответственность, поставщик транспорта задает **свойство PR_RESPONSIBILITY** ([PidTagResponsibility),](pidtagresponsibility-canonical-property.md)а затем возвращает.
    
4. Поставщик транспорта может использовать метод [IMAPISupport::StatusRecips,](imapisupport-statusrecips.md) чтобы указать, распознает ли он получателей, которые не удается доставить, или создать стандартный отчет о доставке. **StatusRecips** — это удобный способ для поставщиков транспорта, которые определили, что некоторые получатели не могут быть доставлены или получили сведения о доставке из своей системы обмена сообщениями, которые могут оказаться полезными для пользователя или клиентского приложения. 
    
5. Вызов поставщика услуг пула MAPI к [IXPLogon::EndMessage](ixplogon-endmessage.md) — это окончательная ответственность за передачу сообщения из пула MAPI поставщику транспорта. 
    
6. Пулер MAPI может использовать [IXPLogon::TransportNotify](ixplogon-transportnotify.md) для отмены обработки сообщений во время вызовов **SubmitMessage** или **EndMessage.** 
    

