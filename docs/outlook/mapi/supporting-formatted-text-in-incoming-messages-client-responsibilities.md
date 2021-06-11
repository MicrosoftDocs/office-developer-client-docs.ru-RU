---
title: Поддержка отформатированный текст в входящих сообщениях клиентские обязанности
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
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>Поддержка форматного текста в входящих сообщениях: клиентские обязанности

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
По мере передачи сообщений между системами обмена сообщениями spooler MAPI позволяет синхронизировать форматирование текста с текстом сообщения. Spooler MAPI вызывает [функцию RTFSync](rtfsync.md) из завернутой версии сообщения, которое передается поставщику транспорта. Поставщик транспорта сохраняет изменения, внесенные в сообщение, вызывая [метод IMAPIProp::SaveChanges,](imapiprop-savechanges.md) а затем передает его новому получателю. 
  
Когда клиентное приложение получателя с RTF открывает сообщение для отображения текста, оно должно синхронизировать текст с форматированием и открыть либо **PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)или **PR_BODY** [(PidTagBody),](pidtagbody-canonical-property.md)в зависимости от того, какое свойство доступно.
  
 **Чтобы открыть сообщение, клиенты, осведомленные о RTF**
  
1. Позвоните **в RTFSync,** чтобы синхронизировать текст сообщения с форматированием, если хранилище сообщений не знает RTF. Флаг RTF_SYNC_BODY_CHANGED должен быть передан в _параметре ulFlags,_ если свойство [PR_RTF_IN_SYNC (PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)отсутствует или настроено на FALSE.  Клиенты, работающие с RTF-магазинами сообщений, не должны вызывать **RTFSync,** так как магазин сообщений позаботится об этом. 
    
2. Вызов [IMAPIProp::SaveChanges,](imapiprop-savechanges.md) если текст сообщения обновлен. 
    
3. Чтобы открыть свойство PR_RTF_COMPRESSED, позвоните в [IMAPIProp::OpenProperty.](imapiprop-openproperty.md)  Если **PR_RTF_COMPRESSED** недоступна, необходимо открыть свойство **PR_BODY** для отображения контента сообщения. 
    
4. Вызов [функции WrapCompressedRTFStream](wrapcompressedrtfstream.md) для создания некомпрессивной версии сжатых данных RTF, если это доступно. 
    
5. Отображение пользователю незапечатаных данных RTF или обычных текстовых данных.
    
 **RTFSync** возвращает значение Boolean, которое указывает, обновлено ли сообщение. Если это значение возвращает ЗНАЧЕНИЕ TRUE, в какой-то момент позвоните **в SaveChanges,** чтобы сделать обновление постоянным. Вызов не должен быть выполнен сразу после **возвращения RTFSync.** 
  
> [!NOTE]
> Поскольку перед его получением многие компоненты обрабатывают отформатированный текст, существует вероятность повреждения. Эта коррупция может происходить от поставщика магазина сообщений, сторонних приложений, шлюза или ошибки передачи. 
  

