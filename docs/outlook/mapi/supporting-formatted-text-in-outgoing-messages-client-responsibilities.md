---
title: Поддержка форматного текста в обязанностях клиента исходящих сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431605"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Поддержка форматного текста в исходящих сообщениях: клиентские обязанности

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения устанавливают **свойство PR_BODY** [(PidTagBody),](pidtagbody-canonical-property.md) **свойство PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)или **свойство PR_HTML** [(PidTagHtml)](pidtaghtml-canonical-property.md)для исходяшего сообщения. Клиенты, поддерживают только простой текст, за набором **только PR_BODY** свойства. Клиенты с богатым текстовым форматом (RTF) могут устанавливать свойства PR_BODY и **PR_RTF_COMPRESSED** или только PR_RTF_COMPRESSED **в** зависимости от используемого поставщика магазина сообщений.  Клиенты, осведомленные о **HTML, PR_HTML** свойство. 
  
Важно, чтобы клиент проверил свойство PR_STORE_SUPPORT_MASK  магазина сообщений[(PidTagStoreSupportMask),](pidtagstoresupportmask-canonical-property.md)чтобы определить, поддерживает ли магазин RTF. Если хранилище сообщений не известно о RTF, клиент, осведомленный о RTF, задает свойства PR_BODY **PR_RTF_COMPRESSED** для каждого исходяшего сообщения.  
  
Если хранилище сообщений RTF-известно,  необходимо PR_RTF_COMPRESSED только свойство. 
  
 **Чтобы установить PR_RTF_COMPRESSED и убедиться, что процесс синхронизации происходит при необходимости, клиенты, осведомленные о RTF**
  
1. Чтобы открыть свойство PR_RTF_COMPRESSED, вызовите метод [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) MAPI_CREATE и MAPI_MODIFY флаги.  MAPI_CREATE гарантирует, что любые новые данные заменяют старые данные, а MAPI_MODIFY позволяет делать эти замены. 
    
2. Вызов функции [WrapCompressedRTFStream,](wrapcompressedrtfstream.md) STORE_UNCOMPRESSED_RTF если хранилище сообщений задает STORE_UNCOMPRESSED_RTF в свойстве **PR_STORE_SUPPORT_MASK,** чтобы получить ненапечатаемую версию потока PR_RTF_COMPRESSED, возвращаемого из **OpenProperty.** 
    
3. Записывайте текстовые данные сообщения в некомпрессивный поток, возвращаемый из **WrapCompressedRTFStream.**
    
4. Фиксация и освобождение некомпрессивных и сжатых потоков.
    
На данный момент, если поставщик магазина сообщений поддерживает RTF, вы сделали все, что требуется. Вы можете зависеть от поставщика магазина сообщений для обработки  процесса синхронизации и создания свойства PR_BODY, если это необходимо. Однако если поставщик магазина сообщений не поддерживает RTF, необходимо вызвать функцию [RTFSync,](rtfsync.md) чтобы синхронизировать текст с форматированием, установив флаг RTF_SYNC_RTF_CHANGED. 
  

