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
ms.openlocfilehash: d34168743926681ee7169a593e302755b193aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577046"
---
# <a name="writing-uncompressed-formatted-text"></a>Написание несжатого форматированного текста

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
При подготовке к отправить сообщение с форматированный текст, либо свойства сообщения **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) в сжатых или несжатых текст. Написание сжатый текст в свойстве **PR_RTF_COMPRESSED** является очень ЦП и может существенно повлиять на производительность. 
  
Для повышения эффективности отправки сообщения в формате, либо:
  
- Обновите Процессор, решения, не всегда означает ли.
    
    - Или -
    
- Написание несжатую текст в свойстве **PR_RTF_COMPRESSED** . 
    
Процедура настройки **PR_RTF_COMPRESSED** с текстом несжатую — это то же, как для задания с сжатого текста, за исключением. При вызове [WrapCompressedRTFStream](wrapcompressedrtfstream.md), задайте в параметре _ulFlags_ флаг STORE_UNCOMPRESSED_RTF. Установка несжатую текст имеет недостаток, в том, что увеличение размера сообщения. 
  

