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
  
Несмотря на то, что некоторые сообщения состоят только из списка получателей и строки темы, содержимое большинства сообщений, в частности, IPM. Обратите внимание, что в сообщениях есть текст. Текст сообщения может быть простым или форматированным и храниться в трех свойствах: **\_Body** ([PidTagBody](pidtagbody-canonical-property.md)) **,\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) и **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Если ваш клиент является обычным текстовым, задайте **текст\_** для поля Цена. Если вы поддерживаете форматирование текста в формате RTF, задайте либо **PR_RTF_COMPRESSED** только, либо **PR_RTF_COMPRESSED** и **\_текст**, в зависимости от используемого поставщика хранилища сообщений. Когда клиент, поддерживающий RTF, использует хранилище сообщений с поддержкой RTF, он задается только **PR_RTF_COMPRESSED** . Когда клиент с поддержкой RTF использует хранилище сообщений, не поддерживающий RTF, он задает оба свойства. Если ваш клиент поддерживает HTML, задайте свойство **PR_HTML** . 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Определение того, поддерживает ли хранилище сообщений форматированный текст
  
1. Вызовите метод [IMAPIProp::-PROPS](imapiprop-getprops.md) хранилища сообщений для получения свойства **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
    
2. Проверьте STORE_RTF_OK бит. Если установлен STORE_RTF_OK, то поставщик хранилища сообщений поддерживает текст RTF. Если оно не задано, то поставщик хранилища сообщений поддерживает только обычный текст.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Определение того, поддерживает ли ваше хранилище сообщений HTML
  
1. Вызовите метод [IMAPIProp::/PROPS](imapiprop-getprops.md) хранилища сообщений для получения свойства **PR_STORE_SUPPORT_MASK** . 
    
2. Проверьте STORE_HTML_OK бит. Если установлен STORE_HTML_OK, то поставщик хранилища сообщений поддерживает HTML-текст. 
    
## <a name="set-pr_rtf_compressed"></a>Настройка RTF_COMPRESSED\_PR
  
1. Вызовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **PR_RTF_COMPRESSED** , указав IID_IStream в качестве идентификатора интерфейса и установив флаг MAPI_CREATE. 
    
2. Вызовите функцию [врапкомпресседртфстреам](wrapcompressedrtfstream.md) , передав флаг STORE_UNCOMPRESSED_RTF, если STORE_UNCOMPRESSED_RTF бит задан в свойстве **PR_STORE_SUPPORT_MASK** хранилища сообщений. 
    
3. Освободите исходный поток, вызвав его метод * * IUnknown:: Release * *. 
    
4. Call — * * IStream:: Write * * или **IStream:: CopyTo** для записи текста сообщения в поток, возвращенный из **врапкомпресседртфстреам**.
    
5. Вызовите методы **commit** и **Release** в потоке, возвращенном из метода **опенпроперти** . 
    
На этом шаге, если поставщик хранилища сообщений поддерживает RTF, вы выполнили все необходимые действия. Вы можете зависеть от поставщика хранилища сообщений, чтобы обрабатывать синхронизацию содержимого и форматирования сообщения и при необходимости создавать **свойство\_текста PR** . Хранилища сообщений с поддержкой RTF [ртфсинк](rtfsync.md) вызовов для обработки синхронизации. Если флаг SYNC_BODY_CHANGED\_RTF имеет значение true, то поставщик повторно вычисляет свойство **PR_BODY** . 
  
Если поставщик хранилища сообщений не поддерживает формат RTF, необходимо также добавить содержимое сообщений, не включенных в формат RTF, с помощью свойства **PR_BODY** . 
  
## <a name="set-pr_html"></a>Настройка PR_HTML
  
1. Вызовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **PR_HTML** с интерфейсом **IStream** . 
    
2. Call **IStream:: Write** для записи текстовых данных сообщения в поток, возвращенный из **опенпроперти**. 
    
3. Вызов **IStream:: Commit** and **IUnknown:: Release** в потоке для фиксации изменений и освобождения памяти. 
    
## <a name="set-pr_body"></a>Настройка PR_BODY
  
1. Вызовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **PR_BODY** с интерфейсом **IStream** . 
    
2. Call **IStream:: Write** для записи текстовых данных сообщения в поток, возвращенный из **опенпроперти**. 
    
3. Вызовите функцию [ртфсинк](rtfsync.md) для синхронизации текста с форматированием. Так как это новое сообщение, установите флаги RTF_SYNC_RTF_CHANGED и RTF_SYNC_BODY_CHANGED, чтобы указать, что текст сообщения был изменен как в формате RTF, так и в виде обычного текста. **Ртфсинк** задаст несколько связанных свойств, необходимых поставщику хранилища сообщений, например **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), и запишите их в сообщение.
    
4. Вызов **IStream:: Commit** and **IUnknown:: Release** в потоке для фиксации изменений и освобождения памяти. 
    

