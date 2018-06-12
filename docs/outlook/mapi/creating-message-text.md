---
title: Создание текста сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 38be3bc2df8931ca45da12e43436377545e8a977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808265"
---
# <a name="creating-message-text"></a>Создание текста сообщения

**Применимо к**: Outlook 
  
Несмотря на то, что некоторые сообщения состоят из не более чем список получателей и Тема содержимого большинство сообщений, в частности IPM. Обратите внимание, сообщения, включает в себя текст. Сообщение может быть обычным или форматированный текст и хранится в три свойства: **связей с Общественностью\_ТЕЛО** ([PidTagBody](pidtagbody-canonical-property.md)), **связей с Общественностью\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) и **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 

Если ваш клиент на основе обычного текста, установите **связей с Общественностью\_ТЕЛО**. Если вы поддерживаете форматированный текст в форматированный текст (RTF), необходимо задать только **PR_RTF_COMPRESSED** или оба **PR_RTF_COMPRESSED** и **связей с Общественностью\_ТЕЛО**, в зависимости от поставщика хранилища сообщений, которое используется. Если принять во внимание RTF клиент использует принять во внимание RTF хранилища сообщений, **PR_RTF_COMPRESSED** задает только. Когда принять во внимание RTF клиент использует хранилище поддерживающими RTF сообщений, задает оба свойства. Если клиент поддерживает HTML, присвойте свойству **PR_HTML** . 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>Определить, поддерживает ли хранения сообщений формат RTF
  
1. Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) хранилище сообщений для получения свойства **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).
    
2. Проверьте наличие бит STORE_RTF_OK. Если значение STORE_RTF_OK, поставщик хранения сообщений поддерживает текст RTF. Если не указано, поставщик хранения сообщений поддерживает только обычный текст.
    
## <a name="determine-whether-your-message-store-supports-html"></a>Определить, поддерживает ли хранения сообщений HTML
  
1. Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) хранилище сообщений для получения свойства **PR_STORE_SUPPORT_MASK** . 
    
2. Проверьте наличие бит STORE_HTML_OK. Если значение STORE_HTML_OK, поставщик хранения сообщений поддерживает HTML-текст. 
    
## <a name="set-prrtfcompressed"></a>Установка связей с Общественностью\_RTF_COMPRESSED
  
1. Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) сообщение, чтобы открыть свойство **PR_RTF_COMPRESSED** , указав IID_IStream идентификатор интерфейса и установка флага MAPI_CREATE. 
    
2. Вызовите функцию [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , передав флаг STORE_UNCOMPRESSED_RTF, если STORE_UNCOMPRESSED_RTF бит задан в свойстве **PR_STORE_SUPPORT_MASK** хранилища сообщений. 
    
3. Освобождение исходный поток, вызвав его ** функции IUnknown::Release ** метод. 
    
4. Вызвать ** IStream::Write ** или **IStream::CopyTo** для записи текста сообщения в потоке, возвращенный из **WrapCompressedRTFStream**.
    
5. Вызовите методы **Фиксация** и **выпуска** для потока, возвращенный методом **OpenProperty** . 
    
На этом этапе Если поставщик хранения сообщений поддерживает RTF, выполнен все, что является обязательным. Может зависеть от поставщика хранилища сообщений для обработки форматирование и синхронизация содержимого сообщений и для создания **связей с Общественностью\_ТЕЛО** свойства, если это необходимо. Хранилищ принять во внимание RTF сообщений вызов [RTFSync](rtfsync.md) для обработки синхронизации. Если RTF\_флаг SYNC_BODY_CHANGED имеет значение TRUE, поставщик будет пересчитывать свойства **PR_BODY** . 
  
Если поставщик хранилища сообщений не поддерживает формат RTF, необходимо также добавить содержимое сообщения не RTF путем установки свойства **PR_BODY** . 
  
## <a name="set-prhtml"></a>Набор PR_HTML
  
1. Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , чтобы открыть **PR_HTML** свойства с помощью интерфейса **IStream** . 
    
2. Вызов **IStream::Write** для записи данных текста сообщения в поток, возвращенный **OpenProperty**. 
    
3. Вызовите **IStream::Commit** и **функции IUnknown::Release** потока, чтобы сохранить изменения и освобождать память. 
    
## <a name="set-prbody"></a>Набор PR_BODY
  
1. Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , чтобы открыть **PR_BODY** свойства с помощью интерфейса **IStream** . 
    
2. Вызов **IStream::Write** для записи данных текста сообщения в поток, возвращенный **OpenProperty**. 
    
3. Вызовите функцию [RTFSync](rtfsync.md) , чтобы синхронизировать текст с форматированием. Поскольку это новое сообщение, задайте RTF_SYNC_RTF_CHANGED и RTF_SYNC_BODY_CHANGED флаги для указания, что изменения RTF и обычного текста версия текста сообщения. **RTFSync** будет установка нескольких связанных свойств, которые требуется поставщик хранения сообщений, таких как **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) и записи их к сообщению.
    
4. Вызовите **IStream::Commit** и **функции IUnknown::Release** потока, чтобы сохранить изменения и освобождать память. 
    

