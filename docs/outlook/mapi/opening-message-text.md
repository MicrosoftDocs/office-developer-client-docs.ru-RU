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
  
Текст сообщения хранится в свойстве **PR \_ BODY** или **PR \_ RTF \_ COMPRESSED.** Дополнительные сведения см. в PR **\_ BODY** ([PidTagBody),](pidtagbody-canonical-property.md) **PR \_ HTML** ([PidTagHtml)](pidtaghtml-canonical-property.md)и **PR \_ RTF \_ COMPRESSED** ([PidTagRtfCompressed).](pidtagrtfcompressed-canonical-property.md) 

Если вы поддерживаете формат RTF, откройте **\_ pr-RTF_COMPRESSED.** Если вы не поддерживаете RTF, откройте **PR \_ BODY.** Так как текст сообщения может быть большим независимо от того, отформатирован ли он, используйте **IMAPIProp::OpenProperty,** чтобы открыть эти свойства. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Отображение форматированный текст сообщения
  
1. Если вы используете хранилище сообщений без RTF, о чем свидетельствует отсутствие флага STORE_RTF_OK в свойстве PR_STORE_SUPPORT_MASK магазина **(** [PidTagStoreSupportMask):](pidtagstoresupportmask-canonical-property.md)
    
    1. Вызовите метод **IMAPIProp::GetProps** сообщения, чтобы PR_RTF_IN_SYNC **свойства.** Дополнительные сведения см. в подразделе [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync).](pidtagrtfinsync-canonical-property.md)
        
    2. Вызовите RTFSync, чтобы синхронизировать свойство PR_BODY сообщения со **свойством PR_RTF_COMPRESSED.** Дополнительные сведения см. в [RTFSync,](rtfsync.md) **PR_BODY** и **PR_RTF_COMPRESSED.** Передав RTF_SYNC_BODY_CHANGED, если вызов для  извлечения PR_RTF_IN_SYNC не удалось, так как свойство не существует или ему задается false. 
        
    3. Если **RTFSync** вернул true (указывая, что были внесены изменения), вызовите метод **IMAPIProp::SaveChanges** сообщения, чтобы окончательно сохранить их. Дополнительные сведения см. в [подразделе IMAPIProp::SaveChanges.](imapiprop-savechanges.md)
    
2. Независимо от того, используете ли вы хранилище сообщений с RTF:
    
    1. Вызовите **IMAPIProp::OpenProperty,** чтобы открыть **PR_RTF_COMPRESSED** свойства. Дополнительные сведения см. в подразделе [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и **PR_RTF_COMPRESSED.**
        
    2. Если **PR_RTF_COMPRESSED** недоступны, вызовите **OpenProperty,** чтобы открыть **PR_BODY** свойства. 
        
    3. Вызовите **функцию WrapCompressedRTFStream,** чтобы создать несжатую версию сжатых данных RTF, если они доступны. Дополнительные сведения [см. в подраздеке WrapCompressedRTFStream.](wrapcompressedrtfstream.md)
        
    4. Скопируйте отформатированный текст из потока в соответствующее место в форме сообщения. 
    
### <a name="to-display-plain-message-text"></a>Отображение обычного текста сообщения
  
1. Вызовите метод **IMAPIProp::GetProps** сообщения, чтобы PR_BODY **свойства.** Дополнительные сведения см. в [подразделе IMAPIProp::GetProps.](imapiprop-getprops.md)
    
2. Если **Метод GetProps** PT_ERROR для типа свойства в структуре значения свойства или MAPI_E_NOT_ENOUGH_MEMORY, вызовите метод **IMAPIProp::OpenProperty** сообщения. Перед **PR_BODY** в качестве тега свойства и IID_IStream в качестве идентификатора интерфейса. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Скопируйте обычный текст из потока в соответствующее место в форме сообщения. 
    

