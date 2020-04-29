---
title: Написание несжатого форматированного текста
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426326"
---
# <a name="writing-uncompressed-formatted-text"></a>Написание несжатого форматированного текста

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
При подготовке к отправке сообщения с форматированным текстом установите для свойства **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) значение сжатый или несжатый текст. Запись сжатого текста в свойстве **PR_RTF_COMPRESSED** является очень трудоемкой операцией ЦП и может значительно повлиять на производительность. 
  
Чтобы увеличить производительность при отправке отформатированных сообщений, выполните одно из следующих действий.
  
- Обновление ЦП, решение, которое не всегда плаусибле.
    
    - Также
    
- Запись несжатого текста в свойстве **PR_RTF_COMPRESSED** . 
    
Процедура установки **PR_RTF_COMPRESSED** с несжатым текстом аналогична процедуре для настройки сжатого текста с одним исключением. При вызове [врапкомпресседртфстреам](wrapcompressedrtfstream.md)установите флаг STORE_UNCOMPRESSED_RTF в параметре _ulFlags_ . Недостаток несжатого текста имеет недостаток в том, что он увеличивает размер сообщений. 
  

