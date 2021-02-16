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
  
Существует две возможные кодировки для содержимого сообщения: одна с использованием MIME, другая — uuencode. Предпочтительным является кодивка MIME. Кроме того, MAPI определяет свойство для каждого **получателя PR_SEND_RICH_INFO** ([PidTagSendRichInfo),](pidtagsendrichinfo-canonical-property.md)которое определяет, следует ли включать сведения в TNEF в исходящую информацию. Таким образом, существует четыре способа кодив содержимого сообщений:
  
- MIME с TNEF
    
- MIME без TNEF
    
- uuencode с TNEF
    
- uuencode без TNEF
    
Как выбрать MIME или uuencode для исходящие сообщения, не указано.
  
Из TNEF исключаются следующие свойства: **PR_SENDER_, \*** **PR_ATTACH_DATA_ \***, **PR_BODY**. Все остальные свойства передаваемых сообщений включаются в поток TNEF.
  
Следующие предложения предназначены для предоставления списка параметров, которые реализация может решить, как поддерживать:
  
- Следует ли кодировать исходящие сообщения с помощью MIME или uuencode: boolean.
    
- Набор символов для исходящие сообщения: строка (скопированная непосредственно в параметр charset) или enumeration (преобразуемая внутри организации в строку charset).
    

