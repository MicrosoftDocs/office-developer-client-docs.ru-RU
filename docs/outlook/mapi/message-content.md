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
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435462"
---
# <a name="message-content"></a>Содержимое сообщения

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Существует две возможные кодировки для содержимого сообщения: один использует MIME, другой с помощью кодировки UUENCODE. Кодировка MIME предпочтительна. Кроме того, MAPI определяет свойство для каждого получателя, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), которое определяет, следует ли включать в исходящие сообщения сведения TNEF. Таким образом, существует четыре способа кодирования содержимого сообщений:
  
- MIME с форматом TNEF
    
- MIME без формата TNEF
    
- Кодировка uuencode с форматом TNEF
    
- Кодировка uuencode без формата TNEF
    
Не указано, как выбрать MIME или uuencode для исходящих сообщений.
  
Следующие свойства исключены из TNEF: **\*PR_SENDER_**, **PR_ATTACH_DATA_\*** **PR_BODY**. Все другие свойства передающего сообщение включены в поток TNEF.
  
Приведенные ниже рекомендации предназначены для предоставления списка параметров, которые может решить реализация:
  
- Необходимость кодирования исходящих сообщений с помощью MIME или uuencode: Boolean.
    
- Набор символов, используемый для исходящих сообщений: строка (копируется непосредственно в параметр CharSet) или перечисление (внутреннее преобразование осуществляется в строку Charset).
    

