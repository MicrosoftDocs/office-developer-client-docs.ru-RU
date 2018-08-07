---
title: Содержимое сообщения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5e8debcd5a60357f05dfb7b6bde1faf972e50a26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810010"
---
# <a name="message-content"></a>Содержимое сообщения

  
  
**Относится к**: Outlook 
  
Существует два возможных кодировки для содержимого сообщения: один с помощью MIME, другой с помощью uuencode. MIME — это кодировки. В дополнение к этому MAPI определяет свойство каждого получателя, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), который управляет ли данные TNEF должно быть включено в исходящих сообщений. Так что являются всего четыре способа кодирования содержимого сообщения:
  
- MIME с TNEF
    
- MIME-без TNEF
    
- UUENCODE с TNEF
    
- UUENCODE без TNEF
    
Выбор MIME и uuencode исходящих сообщений не указан.
  
Следующие свойства, исключаются из формата TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**. Все остальные свойства передаваемого сообщения включаются в поток TNEF.
  
Следующие рекомендации предназначены для предоставления списка параметров, которые реализации можно решить, как обеспечить поддержку:
  
- Следует ли кодирование, используя MIME и uuencode для исходящих сообщений: boolean.
    
- Кодировка исходящих сообщений: string (копируется непосредственно в параметр charset) или перечисление (внутреннее преобразование строку знаков).
    

