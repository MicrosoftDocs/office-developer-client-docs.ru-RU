---
title: Отправка сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 01fd66033da0f24948913f47a752d555eca655fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423624"
---
# <a name="sending-a-message"></a>Отправка сообщения

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Когда вы готовы отправить сообщение, позвоните по методу [IMessage::SubmitMessage.](imessage-submitmessage.md) **SubmitMessage** помещает сообщение в исходячую очередь и задает флаг MSGFLAG_SUBMIT в  свойстве [PR_MESSAGE_FLAGS (PidTagMessageFlags).](pidtagmessageflags-canonical-property.md)
  
Поставщик хранения сообщений, если он тесно связан с поставщиком транспорта, передает сообщение непосредственно транспорту, который доставляет его в систему обмена сообщениями. Если это не тесно, поставщик магазина сообщений информирует spooler MAPI о том, что исходяя очередь изменилась, а пуллер MAPI передает сообщение соответствующему поставщику транспорта.
  
Если вы позволите пользователям отменить операцию отправки, позвоните [в IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) для реализации этой функции. **AbortSubmit** удаляет сообщение из исходявой очереди. Пользователям может быть разрешено остановить отправку до тех пор, пока сообщение не будет передано в систему обмена сообщениями. 
  
Если **SubmitMessage** возвращает MAPI_E_CORRUPT_DATA, предположим, что отправленные данные потеряны. Перед повторной отправкой перепишите сообщение, позвонив [в IMAPIProp::SetProps](imapiprop-setprops.md) и [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Отображение ошибки для пользователя, если эти **вызовы IMAPIProp** сбой или **если SubmitMessage** не во второй раз. 
  
После успешного вызова **в SubmitMessage** освободите любую память, выделенную для списка получателей, и освободите сообщение и его вложения. После отправления сообщения MAPI не разрешает дальнейшие операции в указателях для этих объектов. Исключением является вызов **IUnknown::Release**. Другие вызовы не допускаются, так как многие поставщики магазинов сообщений недействительны идентификаторы записей для отправленных сообщений.
  

