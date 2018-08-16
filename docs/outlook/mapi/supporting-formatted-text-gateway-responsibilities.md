---
title: Поддержка обязанности шлюза форматированного текста
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6d2c85aa76a372ba79e55dbf5b22024288214df6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812417"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>Поддержка форматированного текста: обязанности шлюза

  
  
**Относится к**: Outlook 
  
 **Для обработки формат RTF для исходящих сообщений, шлюзов**
  
1. Извлечение только свойство message **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) из хранилища сообщений. Основное преимущество для извлечения только свойство **PR_RTF_COMPRESSED** — это, что текста сообщения не обязательно должна отправляться между компьютерами, если существует шлюз и хранилища сообщений на разных компьютерах. 
    
2. Создание текста сообщения из форматированный текст, либо с помощью вызова функции библиотека RTF **HrTextFromCompressedRTFStream** или, если сообщение хранятся **RTFSync**. Флаг RTF_SYNC_RTF_CHANGED должен быть установлен в вызове **RTFSync**. Для получения дополнительных сведений см [RTFSync](rtfsync.md).
    
3. Любые изменения нельзя обратить к тексту сообщения, например удаление неподдерживаемые символы. 
    
4. Убедитесь, что **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) и все свойства auxilliary RTF — либо набор или отсутствует.
    
5. После внесения каких-либо изменений вызовов **RTFSync** с набором флаги RTF_SYNC_RTF_CHANGED и RTF_SYNC_BODY_CHANGED. **RTFSync** будет пересчитывать свойства auxilliary RTF из измененного текста. 
    
6. Любые изменения reversable текста сообщения, такие как вставка заполнители вложения и выполняется преобразование обратимое кодовой страницы.
    
7. Отправьте сообщение.
    
 **Для обработки формат RTF для входящих сообщений, шлюзов**
  
1. Обратные каких-либо изменений текста сообщения, которые были внесены непосредственно перед отправкой сообщения. 
    
2. Вызовите **RTFSync** , если сообщение содержит свойства **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) и **PR_RTF_COMPRESSED** . 
    
3. Обновить сообщения в хранилище сообщений с помощью свойства **PR_RTF_COMPRESSED** , если сообщение содержит обновление с помощью свойства **PR_BODY** только в том случае, если отсутствует **PR_RTF_COMPRESSED** . 
    
4. Отменить **PR_BODY** , если сообщение содержит то, как это свойство, так и для **PR_RTF_COMPRESSED**.
    
Шлюзы вызовите **RTFSync** , чтобы избежать передачи текста сообщения и форматированный текст, если хранилище сообщений на другом компьютере. Если шлюз является локальным, его эти свойства и разрешить хранилище сообщений синхронизации. 
  
