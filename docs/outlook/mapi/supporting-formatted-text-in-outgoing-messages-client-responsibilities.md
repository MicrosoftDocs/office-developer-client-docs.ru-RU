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
ms.openlocfilehash: 975dd172b6ad342351f014d0966d62a150f713c6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571292"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>Поддержка форматированного текста в исходящих сообщениях: обязанности клиентов

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Клиентские приложения задать свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) или свойство **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) для исходящих сообщений. Клиенты, которые поддерживают только обычного текста для свойства только **PR_BODY** . Текст в формате RTF (RTF)-принять во внимание, клиенты могут установить **PR_BODY** и **PR_RTF_COMPRESSED** свойства, или только **PR_RTF_COMPRESSED**, в зависимости от сообщения сохраняются используемого поставщика. Клиенты с поддержкой HTML необходимо задать свойство **PR_HTML** . 
  
Важно, чтобы клиент мог свойство **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) хранилища сообщений, чтобы определить, поддерживает ли хранилище RTF. Если хранилище сообщений не принять во внимание RTF, поддерживающую RTF клиента задает свойства как **PR_BODY** , так и **PR_RTF_COMPRESSED** для всех исходящих сообщений. 
  
Если принять во внимание RTF хранилища сообщений, только свойство **PR_RTF_COMPRESSED** необходимо задать. 
  
 **Для задания PR_RTF_COMPRESSED и убедитесь, что синхронизация процесса возникает при необходимости, поддерживающую RTF клиентов**
  
1. Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для открытия установки флаги MAPI_CREATE и MAPI_MODIFY свойства **PR_RTF_COMPRESSED** . MAPI_CREATE гарантирует, что все новые данные заменяет все старые данные и MAPI_MODIFY позволяет выполнять их замены. 
    
2. Вызовите функцию [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , передав STORE_UNCOMPRESSED_RTF, если хранилище сообщений устанавливает бит STORE_UNCOMPRESSED_RTF в своем свойстве **PR_STORE_SUPPORT_MASK** , чтобы получить несжатую версию **PR_RTF_COMPRESSED **потока, возвращаемые **OpenProperty**.
    
3. Запись данных текста сообщения в несжатую поток, возвращенный из **WrapCompressedRTFStream**.
    
4. Фиксация и выпуска и несжатого потоков.
    
На этом этапе Если поставщик хранения сообщений поддерживает RTF, выполнен все, что является обязательным. Может зависеть от поставщика хранилища сообщений для обработки процесс синхронизации и созданием свойство **PR_BODY** , если это необходимо. Тем не менее если поставщик хранения сообщения не поддерживает формат RTF, необходимо вызвать функцию [RTFSync](rtfsync.md) , чтобы синхронизировать текст с форматированием, установка флага RTF_SYNC_RTF_CHANGED. 
  

