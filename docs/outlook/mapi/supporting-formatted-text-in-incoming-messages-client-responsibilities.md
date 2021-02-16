---
title: Поддержка форматированный текст в обязанности клиента входящих сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434503"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>Поддержка форматированный текст во входящих сообщениях: обязанности клиента

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
При передаче сообщений между системами обмена сообщениями пул MAPI позволяет синхронизировать форматирование форматирования с текстом сообщения. Пулер MAPI вызывает функцию [RTFSync](rtfsync.md) из оболочки сообщения, которое передает поставщику транспорта. Поставщик транспорта сохраняет изменения, внесенные в сообщение, вызывая метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) и перенаправ его новому получателю. 
  
Когда клиентская приложение получателя с RTF открывает сообщение для отображения текста, оно должно синхронизировать текст с форматированием и открыть **PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)или **PR_BODY** ([PidTagBody),](pidtagbody-canonical-property.md)в зависимости от того, какое свойство доступно.
  
 **Чтобы открыть сообщение, клиенты с RTF**
  
1. Вызовите **RTFSync,** чтобы синхронизировать текст сообщения с форматированием, если хранилище сообщений не знает RTF. Флаг RTF_SYNC_BODY_CHANGED должен передаваться в  _параметре ulFlags,_ если свойство **PR_RTF_IN_SYNC** ([PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)отсутствует или задано как FALSE. Клиенты, работающие с хранилищами сообщений с RTF, не должны вызывать **RTFSync,** так как хранилище сообщений об этом позаботится. 
    
2. Вызовите [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) если текст сообщения обновлен. 
    
3. Вызовите [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) чтобы открыть **PR_RTF_COMPRESSED** свойства. Если **PR_RTF_COMPRESSED** недоступны, следует открыть свойство  PR_BODY, чтобы отобразить содержимое сообщения. 
    
4. Вызовите [функцию WrapCompressedRTFStream,](wrapcompressedrtfstream.md) чтобы создать несжатую версию сжатых данных RTF, если они доступны. 
    
5. Отображение несмеченных данных RTF или обычных текстовых данных для пользователя.
    
 **RTFSync** возвращает boolean значение, которое указывает, было ли сообщение обновлено. Если это значение возвращает значение TRUE, вызовите **SaveChanges** в определенный момент, чтобы сделать обновление постоянным. Вызов не нужно делать сразу после возврата **RTFSync.** 
  
> [!NOTE]
> Так как перед его получением многие компоненты обрабатывают отформатированный текст, существует вероятность повреждения. Это может произойть из-за поставщика хранения сообщений, стороннего приложения, шлюза или ошибки передачи. 
  

