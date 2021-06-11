---
title: Создание текста сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5b4a4107d6326a61f50a4023ebc2538f699224b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428006"
---
# <a name="creating-message-text"></a>Создание текста сообщения

**Область применения**: Outlook 2013 | Outlook 2016 
  
Хотя некоторые сообщения состоит не более чем из списка получателей и строки тем, содержимое большинства сообщений, в частности IPM. Примечание сообщений, включая текст. Текст сообщения может быть простым или отформатирован и хранится в трех свойствах: PR **\_ BODY** [(PidTagBody),](pidtagbody-canonical-property.md) **PR \_ HTML** [(PidTagHtml)](pidtaghtml-canonical-property.md)и **PR_RTF_COMPRESSED** [(PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md) 

Если клиент простой на основе текста, установите **PR \_ BODY**. Если вы поддерживаете форматированный текст в формате Rich Text (RTF), установите только PR_RTF_COMPRESSED или PR_RTF_COMPRESSED и **PR \_ BODY**, в зависимости от поставщика магазина сообщений, который вы используете.   Если клиент, осведомленный о RTF, использует хранилище сообщений с RTF, он задает только **PR_RTF_COMPRESSED.** Если клиент, осведомленный о RTF, использует хранилище сообщений, не относя к RTF, оно задает оба свойства. Если клиент поддерживает HTML, установите **свойство** PR_HTML. 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Определите, поддерживает ли ваш магазин сообщений насыщенный текстовый формат
  
1. Чтобы получить свойство[PR_STORE_SUPPORT_MASK PidTagStoreSupportMask,](pidtagstoresupportmask-canonical-property.md)позвоните по методу [IMAPIProp::GetProps](imapiprop-getprops.md) в хранилище сообщений. 
    
2. Проверьте, STORE_RTF_OK бит. Если STORE_RTF_OK установлено, поставщик магазина сообщений поддерживает текст RTF. Если она не установлена, поставщик магазина сообщений поддерживает только простой текст.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Определите, поддерживает ли ваш магазин сообщений HTML
  
1. Чтобы получить свойство PR_STORE_SUPPORT_MASK, позвоните по методу [IMAPIProp::GetProps](imapiprop-getprops.md) **в хранилище** сообщений. 
    
2. Проверьте, STORE_HTML_OK бит. Если STORE_HTML_OK установлен, поставщик магазина сообщений поддерживает HTML-текст. 
    
## <a name="set-pr_rtf_compressed"></a>Установите \_ pr-RTF_COMPRESSED
  
1. Вызывай метод [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) чтобы открыть свойство **PR_RTF_COMPRESSED,** указав IID_IStream в качестве идентификатора интерфейса и MAPI_CREATE флаг. 
    
2. Вызов [функции WrapCompressedRTFStream,](wrapcompressedrtfstream.md) передав флаг STORE_UNCOMPRESSED_RTF, если STORE_UNCOMPRESSED_RTF установлен в свойстве PR_STORE_SUPPORT_MASK магазина **сообщений.** 
    
3. Отпустите исходный поток, назвав его методом IUnknown::Release **. 
    
4. Вызов либо ** IStream::Write ** или **IStream::CopyTo,** чтобы написать текст сообщения в поток, возвращенный из **WrapCompressedRTFStream**.
    
5. Вызов **методов фиксации** **и выпуска** в потоке, возвращаемом из метода **OpenProperty.** 
    
На данный момент, если поставщик магазина сообщений поддерживает RTF, вы сделали все, что требуется. Вы можете зависеть от поставщика магазина сообщений для синхронизации контента и форматирования сообщений и создания **свойства PR \_ BODY** при необходимости. Для обработки синхронизации в хранилищах сообщений, которые известны RTF, вызываем [RTFSync.](rtfsync.md) Если флаг RTF SYNC_BODY_CHANGED true, поставщик будет повторно PR_BODY \_ свойству.  
  
Если поставщик хранения сообщений не поддерживает RTF, необходимо также добавить содержимое  сообщений, не относя PR_BODY RTF. 
  
## <a name="set-pr_html"></a>Настройка PR_HTML
  
1. Вызов метода [IMAPIProp::OpenProperty,](imapiprop-openproperty.md)  чтобы открыть свойство PR_HTML с интерфейсом **IStream.** 
    
2. Call **IStream::Write** для записи текстовых данных сообщения в поток, возвращаемый из **OpenProperty.** 
    
3. Call **IStream::Commit** и **IUnknown::Release** on the stream to commit the changes and free its memory. 
    
## <a name="set-pr_body"></a>Настройка PR_BODY
  
1. Вызов метода [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) **чтобы** открыть свойство PR_BODY с интерфейсом **IStream.** 
    
2. Call **IStream::Write** для записи текстовых данных сообщения в поток, возвращаемый из **OpenProperty.** 
    
3. Вызов [функции RTFSync, чтобы](rtfsync.md) синхронизировать текст с форматированием. Так как это новое сообщение, установите флаги RTF_SYNC_RTF_CHANGED и RTF_SYNC_BODY_CHANGED, чтобы указать, что изменилась как RTF, так и простая текстовая версия текста сообщения. **RTFSync** задает несколько связанных свойств, необходимых поставщику магазина сообщений, например **PR_RTF_IN_SYNC** [(PidTagRtfInSync),](pidtagrtfinsync-canonical-property.md)и напишет их в сообщение.
    
4. Call **IStream::Commit** и **IUnknown::Release** on the stream to commit the changes and free its memory. 
    

