---
title: Открытие текста сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: ad3499cc1ff3bd8b633fa48173ab8455d5d8d124
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810066"
---
# <a name="opening-message-text"></a>Открытие текста сообщения

**Применимо к**: Outlook 
  
Текст сообщения, хранится в его **связей с Общественностью\_ТЕЛО** свойство или **связей с Общественностью\_RTF\_СЖАТЫЙ** свойство. Дополнительные сведения можно **связей с Общественностью\_ТЕЛО** ([PidTagBody](pidtagbody-canonical-property.md)), **связей с Общественностью\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) и **связей с Общественностью\_RTF\_СЖАТЫЙ** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Если вы поддерживаете форматированный текст (RTF), откройте **связей с Общественностью\_RTF_COMPRESSED**. Если вы не поддерживает формат RTF, откройте **связей с Общественностью\_ТЕЛО**. Так как текстовое сообщение могут занимать много места, независимо от того, является ли он имеет формат, используйте **IMAPIProp::OpenProperty** для открытия этих свойств. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
  
### <a name="to-display-formatted-message-text"></a>Чтобы отобразить форматированный текст сообщения
  
1. При использовании хранилища принять во внимание сообщений не RTF, как указано в отсутствие флага STORE_RTF_OK в свойстве магазина **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)):
    
    1. Вызов метода **IMAPIProp::GetProps** сообщения для получения свойства **PR_RTF_IN_SYNC** . Для получения дополнительных сведений см [IMAPIProp::GetProps](imapiprop-getprops.md) и **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).
        
    2. Вызов RTFSync для синхронизации свойство PR_BODY сообщения со свойством **PR_RTF_COMPRESSED** . Для получения дополнительных сведений см [RTFSync](rtfsync.md), **PR_BODY**и **PR_RTF_COMPRESSED**. PASS RTF_SYNC_BODY_CHANGED флаг, если не удалось выполнить вызов для получения **PR_RTF_IN_SYNC** , так как свойство не существует, либо он имеет значение FALSE. 
        
    3. Если **RTFSync** возвращает значение TRUE, указывающего на то, что изменения — вызов метода **IMAPIProp::SaveChanges** сообщение без возможности восстановления их хранения. Для получения дополнительных сведений см [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
    
2. Независимо от того, является ли вы используете принять во внимание RTF сообщение хранения:
    
    1. Вызовите **IMAPIProp::OpenProperty** , чтобы открыть свойство **PR_RTF_COMPRESSED** . Для получения дополнительных сведений см [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и **PR_RTF_COMPRESSED**.
        
    2. Если **PR_RTF_COMPRESSED** не поддерживается, вызовите **OpenProperty** для открытия свойство **PR_BODY** . 
        
    3. Вызовите функцию **WrapCompressedRTFStream** для создания несжатую версию сжатых данных RTF, если он доступен. Для получения дополнительных сведений см [WrapCompressedRTFStream](wrapcompressedrtfstream.md).
        
    4. Скопируйте форматированного текста в потоке в соответствующее место в форме сообщения. 
    
### <a name="to-display-plain-message-text"></a>Для отображения текста обычные сообщения
  
1. Вызов метода **IMAPIProp::GetProps** сообщения для получения свойства **PR_BODY** . Для получения дополнительных сведений см [IMAPIProp::GetProps](imapiprop-getprops.md).
    
2. Если в структуре значение свойства или MAPI_E_NOT_ENOUGH_MEMORY **GetProps** возвращает либо PT_ERROR для типа свойства, вызовите метод **IMAPIProp::OpenProperty** сообщение. Передайте **PR_BODY** как свойство tag и IID_IStream идентификатор интерфейса. For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).
    
3. Скопируйте текст из потока в соответствующее место в форме сообщения. 
    

