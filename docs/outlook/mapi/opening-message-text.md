---
title: Открытие текста сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 305b0534f828ea72c1e116fd38fb8f578062e32e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407538"
---
# <a name="opening-message-text"></a>Открытие текста сообщения

**Относится к**: Outlook 2013 | Outlook 2016 
  
Текст сообщения хранится в свойстве текста по отношению к **тексту (PR)\_** или **сжатом RTF\_\_(пр.)** . Дополнительную информацию можно узнать в **статье\_Body** ([PidTagBody](pidtagbody-canonical-property.md)), **\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) и **сжатом\_RTF\_** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Если вы поддерживаете формат RTF, откройте **RTF_COMPRESSED "пр\_**". Если вы не поддерживаете формат RTF, **откройте\_текст PR**. Так как текст сообщения может быть большим, независимо от того, отформатирован он или нет, используйте **IMAPIProp:: опенпроперти** , чтобы открыть эти свойства. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Отображение форматированного текста сообщения
  
1. Если вы используете хранилище сообщений с поддержкой не в формате RTF, как указано в разделе отсутствие флага STORE_RTF_OK в свойстве **PR_STORE_SUPPORT_MASK** хранилища ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)):
    
    1. Вызовите метод **IMAPIProp::/PROPS** сообщения, чтобы получить свойство **PR_RTF_IN_SYNC** . Дополнительные сведения см. в статье [IMAPIProp::-PROPS](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Вызов Ртфсинк для синхронизации свойства PR_BODY сообщения с помощью свойства **PR_RTF_COMPRESSED** . Дополнительные сведения см. в статье [ртфсинк](rtfsync.md), **PR_BODY**и **PR_RTF_COMPRESSED**. Передайте флаг RTF_SYNC_BODY_CHANGED, если вызов для получения **PR_RTF_IN_SYNC** окончился неудачей, так как свойство не существует или имеет значение false. 
        
    3. Если **ртфсинк** возвращает значение true, указывающее, что были сделаны изменения, вызовите метод **IMAPIProp:: SaveChanges** сообщения, чтобы окончательно сохранить их. Дополнительные сведения см. в разделе [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
    
2. Независимо от того, используется ли хранилище сообщений с поддержкой RTF:
    
    1. Call **IMAPIProp:: опенпроперти** , чтобы открыть свойство **PR_RTF_COMPRESSED** . Дополнительные сведения см. в статье [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) и **PR_RTF_COMPRESSED**.
        
    2. Если **PR_RTF_COMPRESSED** недоступен, вызовите метод **опенпроперти** , чтобы открыть свойство **PR_BODY** . 
        
    3. Вызовите функцию **врапкомпресседртфстреам** , чтобы создать несжатую версию сжатых данных RTF, если они доступны. Дополнительные сведения см. в разделе [врапкомпресседртфстреам](wrapcompressedrtfstream.md).
        
    4. Скопируйте отформатированный текст из потока в соответствующее место формы сообщения. 
    
### <a name="to-display-plain-message-text"></a>Отображение обычного текста сообщения
  
1. Вызовите метод **IMAPIProp::/PROPS** сообщения, чтобы получить свойство **PR_BODY** . Дополнительные сведения см. в статье [IMAPIProp::/PROPS](imapiprop-getprops.md).
    
2. Если **параметр** GetProperty возвращает либо PT_ERROR для типа свойства в структуре значения свойства, либо MAPI_E_NOT_ENOUGH_MEMORY, вызовите метод **IMAPIProp:: опенпроперти** сообщения. Передайте **PR_BODY** в качестве тега свойства и IID_IStream в качестве идентификатора интерфейса. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Скопируйте обычный текст из потока в соответствующее место формы сообщения. 
    

