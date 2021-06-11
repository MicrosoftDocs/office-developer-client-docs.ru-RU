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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отправка сообщений выполняется серией вызовов из пульпера MAPI поставщику транспорта. Вызовы последовательно следуют следующим образом:
  
1. Spooler MAPI вызывает [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), передав экземпляр [IMESSage : IMAPIProp,](imessageimapiprop.md) чтобы начать процесс. 
    
2. Затем поставщик транспорта помещает эталонное значение — идентификатор, определенный транспортом, используемый в будущих ссылках на это сообщение , в расположении, на котором ссылается **в SubmitMessage.**
    
3. Поставщик транспорта имеет доступ к данным сообщений с помощью переданного **экземпляра IMessage.** Для каждого получателя в переданной **службе IMessage,** за которую он принимает ответственность, поставщик транспорта задает **свойство** [PR_RESPONSIBILITY (PidTagResponsibility),](pidtagresponsibility-canonical-property.md)а затем возвращается.
    
4. Поставщик транспорта может использовать метод [IMAPISupport::StatusRecips,](imapisupport-statusrecips.md) чтобы указать, распознает ли он получателей, которые не могут быть доставлены, или создать стандартный отчет о доставке. **StatusRecips** — это удобство для транспортных поставщиков, которые определили, что некоторые из получателей не могут быть доставлены или получили данные о доставке из их системы обмена сообщениями, которые могут оказаться полезными для пользователя или клиентского приложения. 
    
5. Вызов шпалеров MAPI в [IXPLogon::EndMessage](ixplogon-endmessage.md) — это последняя отдача ответственности за сообщение от пулера MAPI поставщику транспорта. 
    
6. Шпалер MAPI может использовать [IXPLogon::TransportNotify](ixplogon-transportnotify.md) для отмены обработки сообщений во время вызовов **SubmitMessage** или **EndMessage.** 
    

