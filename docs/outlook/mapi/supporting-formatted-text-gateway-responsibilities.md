---
title: Поддержка функций форматированные текстовые шлюзы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419431"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>Поддержка форматного текста: обязанности шлюза

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 **Обработка формата "Богатый текст" для исходяющих сообщений, шлюзов**
  
1. Извлекать только свойство **PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)из магазина сообщений. Основное преимущество при сборе  только свойства PR_RTF_COMPRESSED заключается в том, что текст сообщения не должен отправляться между машинами, если шлюз и хранилище сообщений существуют на разных компьютерах. 
    
2. Создание текста сообщения из форматного текста либо путем вызова функции библиотеки RTF **HrTextFromCompressedRTFStream,** либо, если сообщение хранится локально, **RTFSync**. Флаг RTF_SYNC_RTF_CHANGED должен быть установлен в вызове **RTFSync**. Дополнительные сведения см. в [RTFSync.](rtfsync.md)
    
3. Внести любые необратимые изменения в текст сообщения, например отбросить неподтверченные символы. 
    
4. Убедитесь, **что PR_RTF_IN_SYNC** [(PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)и все вспомогательные свойства RTF либо заданы, либо отсутствуют.
    
5. Если были внесены какие-либо изменения, вызывай **RTFSync** с набором RTF_SYNC_RTF_CHANGED и RTF_SYNC_BODY_CHANGED флагов. **RTFSync** пересчитает вспомогательные свойства RTF из измененного текста. 
    
6. Внести любые обратимые изменения в текст сообщения, такие как вставка вложений и выполнение преобразований страниц недеструктивного кода.
    
7. Отправка сообщения.
    
 **Обработка формата "Богатый текст" для входящих сообщений, шлюзов**
  
1. Отменять любые изменения текста сообщения, которые были сделаны непосредственно перед отправлением сообщения. 
    
2. Вызов **RTFSync,** если сообщение  содержит свойства PR_RTF_COMPRESSED **и PR_BODY** [(PidTagBody).](pidtagbody-canonical-property.md) 
    
3. Обновление сообщения в хранилище сообщений с **помощью свойства PR_RTF_COMPRESSED,** если оно содержится в сообщении; обновление с **PR_BODY,** только **если PR_RTF_COMPRESSED** отсутствует. 
    
4. **Откажитесь PR_BODY,** если сообщение содержит как это свойство, так **и PR_RTF_COMPRESSED.**
    
Шлюзы звонят **в RTFSync,** чтобы не передавать текст сообщения и форматированный текст, если хранилище сообщений находится на другом компьютере. Если шлюз локализуется, он может установить оба свойства и разрешить хранилище сообщений выполнять синхронизацию. 
  

