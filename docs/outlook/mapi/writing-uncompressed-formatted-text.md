---
title: Написание несформатированный форматированный текст
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
# <a name="writing-uncompressed-formatted-text"></a>Написание несформатированный форматированный текст

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
При подготовке к отправке сообщения с форматированный текст установите для свойства **PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)сжатие или несжатие текста. Запись сжатого текста в **PR_RTF_COMPRESSED** является очень интенсивной операцией ЦП и может существенно повлиять на производительность. 
  
Чтобы повысить производительность отправки отформатированные сообщения, сформатированные либо:
  
- Обновите ЦП— решение, которое не всегда можно обуявить.
    
    - Или -
    
- Запишите несмеченный текст в **PR_RTF_COMPRESSED.** 
    
Процедура настройки **PR_RTF_COMPRESSED** с несжатием текста та же, что и для установки сжатого текста за одним исключением. При [вызове WrapCompressedRTFStream](wrapcompressedrtfstream.md)установите флаг STORE_UNCOMPRESSED_RTF в параметре _ulFlags._ Недостаток установки несмеченного текста заключается в том, что он увеличивает размер сообщений. 
  

