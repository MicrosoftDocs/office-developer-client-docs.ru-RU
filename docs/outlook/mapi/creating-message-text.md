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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Хотя некоторые сообщения состоит только из списка получателей и строки темы, содержимое большинства сообщений, в частности IPM. Сообщения заметок, включая текст. Текст сообщения может быть простым или отформатированный и хранится в трех свойствах: **PR \_ BODY** ([PidTagBody),](pidtagbody-canonical-property.md) **PR \_ HTML** ([PidTagHtml)](pidtaghtml-canonical-property.md)и **PR_RTF_COMPRESSED** ([PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md) 

Если клиент основан на обычном тексте, установите **PR \_ BODY.** Если вы поддерживаете форматированный текст в формате RTF, установите  PR_RTF_COMPRESSED только PR_RTF_COMPRESSED и **PR \_ BODY** в зависимости от используемого поставщика rtF.  Когда клиент с RTF использует хранилище сообщений с RTF, он PR_RTF_COMPRESSED **только.** Когда клиент с RTF использует хранилище сообщений, не относя оно к RTF, он задает оба свойства. Если ваш клиент поддерживает HTML, за **установите** PR_HTML свойства. 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Определение того, поддерживает ли хранилище сообщений формат RICH Text
  
1. Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) в хранилище сообщений, чтобы получить свойство **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask).](pidtagstoresupportmask-canonical-property.md)
    
2. Проверьте, нет ли STORE_RTF_OK бита. Если STORE_RTF_OK, поставщик rtF поддерживает текст RTF. Если он не установлен, поставщик store сообщений поддерживает только обычный текст.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Определение того, поддерживает ли хранилище сообщений HTML
  
1. Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) PR_STORE_SUPPORT_MASK **сообщения.** 
    
2. Проверьте, нет ли STORE_HTML_OK бита. Если STORE_HTML_OK установлен, поставщик службы хранения сообщений поддерживает HTML-текст. 
    
## <a name="set-pr_rtf_compressed"></a>Настройка \_ pr-RTF_COMPRESSED
  
1. Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) сообщения, чтобы открыть свойство **PR_RTF_COMPRESSED,** указав IID_IStream в качестве идентификатора интерфейса и установив флаг MAPI_CREATE. 
    
2. Вызовите функцию [WrapCompressedRTFStream,](wrapcompressedrtfstream.md) передав флаг STORE_UNCOMPRESSED_RTF, если STORE_UNCOMPRESSED_RTF в свойстве PR_STORE_SUPPORT_MASK хранения **сообщений.** 
    
3. Выпустите исходный поток, вызывая его метод ** IUnknown::Release **. 
    
4. Call either ** IStream::Write ** or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.
    
5. Вызовите **методы Commit** и **Release** в потоке, возвращаемом **методом OpenProperty.** 
    
На этом этапе, если поставщик rtF поддерживает RTF, вы сделали все необходимое. Вы можете в зависимости от поставщика содержимого и форматирования сообщений обрабатывать синхронизацию содержимого и форматирования сообщений, а также при необходимости создавать **свойство PR \_ BODY.** В сообщениях с RTF хранится вызов [RTFSync](rtfsync.md) для обработки синхронизации. Если для флага SYNC_BODY_CHANGED RTF установлено SYNC_BODY_CHANGED true, поставщик перекомпьютерит \_ **PR_BODY** свойства. 
  
Если ваш поставщик RTF не поддерживает RTF, необходимо также добавить содержимое  сообщений, не относя PR_BODY RTF. 
  
## <a name="set-pr_html"></a>Настройка PR_HTML
  
1. Вызовите [метод IMAPIProp::OpenProperty,](imapiprop-openproperty.md) чтобы открыть PR_HTML **с** помощью **интерфейса IStream.** 
    
2. Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**. 
    
3. Вызовите **IStream::Commit** и **IUnknown::Release** в потоке, чтобы зафиксировать изменения и освободить память. 
    
## <a name="set-pr_body"></a>Настройка PR_BODY
  
1. Вызовите [метод IMAPIProp::OpenProperty,](imapiprop-openproperty.md) чтобы открыть PR_BODY **с** помощью **интерфейса IStream.** 
    
2. Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**. 
    
3. Вызовите [функцию RTFSync,](rtfsync.md) чтобы синхронизировать текст с форматированием. Так как это новое сообщение, установите флаги RTF_SYNC_RTF_CHANGED и RTF_SYNC_BODY_CHANGED, чтобы указать, что версия текста сообщения в виде RTF и обычного текста изменились. **RTFSync** задает несколько связанных свойств, необходимых поставщику store сообщений, например **PR_RTF_IN_SYNC** ([PidTagRtfInSync),](pidtagrtfinsync-canonical-property.md)и запишет их в сообщение.
    
4. Вызовите **IStream::Commit** и **IUnknown::Release** в потоке, чтобы зафиксировать изменения и освободить память. 
    

