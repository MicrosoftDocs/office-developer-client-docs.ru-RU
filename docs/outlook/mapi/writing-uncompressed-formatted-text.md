---
title: Написание некомпрессивного форматного текста
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
# <a name="writing-uncompressed-formatted-text"></a>Написание некомпрессивного форматного текста

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
При подготовке к отправке сообщения с отформатированным текстом **задайте** свойство [PR_RTF_COMPRESSED (PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)на сжатый или ненажатый текст. Написание сжатого **текста в свойстве PR_RTF_COMPRESSED** является очень интенсивной операцией ЦП и может резко повлиять на производительность. 
  
Чтобы повысить производительность отправки отформатированные сообщения, либо:
  
- Обновление ЦП , решение, которое не всегда правдоподобно.
    
    - Или -
    
- Записывай некомпрессивный **текст в свойстве PR_RTF_COMPRESSED.** 
    
Процедура настройки **PR_RTF_COMPRESSED** с некомпрессованным текстом такая же, как и для установки его с сжатым текстом, за одним исключением. При [вызове WrapCompressedRTFStream](wrapcompressedrtfstream.md)установите флаг STORE_UNCOMPRESSED_RTF в _параметре ulFlags._ Настройка некомпрессивного текста имеет недостаток в том, что он увеличивает размер сообщений. 
  

