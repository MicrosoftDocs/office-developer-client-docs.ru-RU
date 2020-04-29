---
title: Поддержка форматированного текста в исходящих сообщениях обязанности клиента
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
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Поддержка форматированного текста в исходящих сообщениях: обязанности клиентов

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения задают свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) или свойство **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) для исходящих сообщений. Клиенты, поддерживающие только обычный текст, задают только свойство **PR_BODY** . Клиенты, поддерживающие формат RTF, могут задавать как свойства **PR_BODY** , так и **PR_RTF_COMPRESSED** , или только **PR_RTF_COMPRESSED**, в зависимости от используемого поставщика хранилища сообщений. Клиенты, поддерживающие HTML, задают свойство **PR_HTML** . 
  
Необходимо, чтобы клиент проверит свойство **PR_STORE_SUPPORT_MASK** хранилища сообщений ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), чтобы определить, поддерживает ли хранилище RTF. Если хранилище сообщений не включено в формат RTF, клиент, поддерживающий RTF, задает для каждого исходящего сообщения как свойства **PR_BODY** , так и **PR_RTF_COMPRESSED** . 
  
Если хранилище сообщений включено в формат RTF, необходимо задать только свойство **PR_RTF_COMPRESSED** . 
  
 **Чтобы задать PR_RTF_COMPRESSED и убедиться в том, что процесс синхронизации выполняется по мере необходимости, поддерживающих RTF клиентов**
  
1. Вызовите метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , чтобы открыть свойство **PR_RTF_COMPRESSED** , задав флаги MAPI_CREATE и MAPI_MODIFY. MAPI_CREATE гарантирует, что все новые данные заменяют все старые данные и MAPI_MODIFY позволят выполнить эти замены. 
    
2. Вызовите функцию [врапкомпресседртфстреам](wrapcompressedrtfstream.md) , передав STORE_UNCOMPRESSED_RTF, если хранилище сообщений устанавливает STORE_UNCOMPRESSED_RTF бит в свойстве **PR_STORE_SUPPORT_MASK** , чтобы получить несжатую версию потока **PR_RTF_COMPRESSED** , возвращенного из **опенпроперти**.
    
3. Запись текстовых данных сообщения в несжатый поток, возвращенный из **врапкомпресседртфстреам**.
    
4. Зафиксируйте и освободите несжатые и сжатые потоки.
    
На этом шаге, если поставщик хранилища сообщений поддерживает RTF, вы выполнили все необходимые действия. При необходимости можно зависеть от поставщика хранилища сообщений для обработки процесса синхронизации и создания свойства **PR_BODY** . Однако если поставщик хранилища сообщений не поддерживает формат RTF, необходимо вызвать функцию [ртфсинк](rtfsync.md) для синхронизации текста с форматированием, установив флаг RTF_SYNC_RTF_CHANGED. 
  

