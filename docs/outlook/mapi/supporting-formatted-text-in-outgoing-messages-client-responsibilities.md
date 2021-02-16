---
title: Поддержка форматированный текст в обязанности клиента исходящих сообщений
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
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Поддержка форматированный текст в исходящих сообщениях: обязанности клиента

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения устанавливают свойство **PR_BODY** ([PidTagBody),](pidtagbody-canonical-property.md) **свойство PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)или **свойство PR_HTML** ([PidTagHtml)](pidtaghtml-canonical-property.md)для исходяшего сообщения. Клиенты, которые поддерживают только обычный текст, устанавливают **только PR_BODY** свойства. Клиенты с RTF могут устанавливать свойства  PR_BODY и **PR_RTF_COMPRESSED** или только PR_RTF_COMPRESSED в зависимости от используемого поставщика rtF. Клиенты, которые знают HTML, **PR_HTML** свойства. 
  
Клиенту важно проверить свойство PR_STORE_SUPPORT_MASK[(PidTagStoreSupportMask),](pidtagstoresupportmask-canonical-property.md)чтобы определить, поддерживает ли хранилище RTF.  Если хранилище сообщений не имеет RTF-данных, клиент с  RTF задает свойства PR_BODY и **PR_RTF_COMPRESSED** для каждого исходяшего сообщения. 
  
Если хранилище сообщений имеет RTF-данные, необходимо PR_RTF_COMPRESSED только свойство.  
  
 **Чтобы настроить PR_RTF_COMPRESSED и убедиться, что синхронизация происходит по мере необходимости, клиенты с RTF**
  
1. Вызовите метод [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) чтобы открыть **свойство PR_RTF_COMPRESSED,** установив MAPI_CREATE и MAPI_MODIFY флаги. MAPI_CREATE все новые данные заменяют все старые данные, MAPI_MODIFY позволяет их заменять. 
    
2. Вызовите функцию [WrapCompressedRTFStream,](wrapcompressedrtfstream.md) передав STORE_UNCOMPRESSED_RTF, если хранилище сообщений задает бит STORE_UNCOMPRESSED_RTF в свойстве **PR_STORE_SUPPORT_MASK,** чтобы получить несмещенную версию потока PR_RTF_COMPRESSED, возвращаемого **из OpenProperty.** 
    
3. Запишите текстовые данные сообщения в несхваченный поток, возвращенный **wrapCompressedRTFStream.**
    
4. Зафиксировать и освободить несжатые и сжатые потоки.
    
На этом этапе, если поставщик rtF поддерживает RTF, вы сделали все необходимое. Для обработки процесса синхронизации и создания свойства PR_BODY при  необходимости можно использовать поставщика PR_BODY сообщений. Однако если поставщик RTF не поддерживает RTF, необходимо вызвать функцию [RTFSync,](rtfsync.md) чтобы синхронизировать текст с форматированием, установив флаг RTF_SYNC_RTF_CHANGED. 
  

