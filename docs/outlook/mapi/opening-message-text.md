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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Текст сообщения хранится либо в свойстве **PR \_ BODY,** либо **в свойстве PR \_ RTF \_ COMPRESSED.** Дополнительные сведения см. в pr **\_ BODY** [(PidTagBody),](pidtagbody-canonical-property.md) **PR \_ HTML** [(PidTagHtml)](pidtaghtml-canonical-property.md)и **PR \_ RTF \_ COMPRESSED** [(PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md) 

Если вы поддерживаете формат Rich Text (RTF), откройте **\_ PR-RTF_COMPRESSED**. Если вы не поддерживаете RTF, откройте **PR \_ BODY**. Поскольку текст сообщения может быть большим независимо от формата или нет, используйте **IMAPIProp::OpenProperty** для открытия этих свойств. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Отображение отформатированный текст сообщения
  
1. Если вы используете хранилище сообщений, не вступив в RTF, о чем свидетельствует  отсутствие флага STORE_RTF_OK в свойстве PR_STORE_SUPPORT_MASK магазина[(PidTagStoreSupportMask):](pidtagstoresupportmask-canonical-property.md)
    
    1. Чтобы получить свойство PR_RTF_IN_SYNC, позвоните по методу **IMAPIProp::GetProps.**  Дополнительные сведения см. [в странице IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** [(PidTagRtfInSync).](pidtagrtfinsync-canonical-property.md)
        
    2. Позвоните в RTFSync, чтобы синхронизировать свойство PR_BODY сообщения с **свойством PR_RTF_COMPRESSED.** Дополнительные сведения см. в [RTFSync,](rtfsync.md) **PR_BODY** и **PR_RTF_COMPRESSED**. Передай флаг RTF_SYNC_BODY_CHANGED, если вызов  на PR_RTF_IN_SYNC не удалось, так как свойство не существует или задано false. 
        
    3. Если **RTFSync** вернул TRUE , указав, что были внесены изменения, позвоните по методу **IMAPIProp::SaveChanges** для их постоянного хранения. Дополнительные сведения см. [в iMAPIProp::SaveChanges.](imapiprop-savechanges.md)
    
2. Независимо от того, используете ли вы хранилище сообщений, в курсе RTF:
    
    1. Чтобы открыть свойство PR_RTF_COMPRESSED, позвоните в **IMAPIProp::OpenProperty.**  Дополнительные сведения см. [в iMAPIProp::OpenProperty](imapiprop-openproperty.md) **и PR_RTF_COMPRESSED.**
        
    2. Если **PR_RTF_COMPRESSED** недоступны, позвоните **в OpenProperty,** чтобы открыть **свойство PR_BODY.** 
        
    3. Вызов **функции WrapCompressedRTFStream** для создания некомпрессивной версии сжатых данных RTF, если это доступно. Дополнительные сведения см. в [ссылке WrapCompressedRTFStream.](wrapcompressedrtfstream.md)
        
    4. Скопируйте отформатированный текст из потока в соответствующее место в форме сообщения. 
    
### <a name="to-display-plain-message-text"></a>Отображение простого текста сообщения
  
1. Чтобы получить свойство PR_BODY, позвоните по методу **IMAPIProp::GetProps.**  Дополнительные сведения см. [в iMAPIProp::GetProps.](imapiprop-getprops.md)
    
2. Если **GetProps** возвращает PT_ERROR для типа свойства в структуре значения свойства или MAPI_E_NOT_ENOUGH_MEMORY, позвоните в **метод IMAPIProp::OpenProperty.** **Передай PR_BODY** как тег свойства и IID_IStream как идентификатор интерфейса. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Скопируйте простой текст из потока в соответствующее место в форме сообщения. 
    

