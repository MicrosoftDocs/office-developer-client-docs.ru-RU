---
title: Содержимое сообщений
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
# <a name="message-content"></a>Содержимое сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Существует два возможных кодирования контента сообщений: одна — с помощью MIME, другая — с помощью uuencode. MIME является предпочтительным кодом. Кроме того, MAPI определяет свойство на одного получателя **PR_SEND_RICH_INFO** [(PidTagSendRichInfo),](pidtagsendrichinfo-canonical-property.md)которое определяет, следует ли включать сведения TNEF в исходящую информацию. Таким образом, существует в общей сложности четыре способа кодить содержимое сообщений:
  
- MIME с TNEF
    
- MIME без TNEF
    
- uuencode с TNEF
    
- uuencode без TNEF
    
Как выбрать MIME или uuencode для исходящие сообщения, не указывается.
  
Из TNEF исключаются следующие свойства: **PR_SENDER_, \*** **PR_ATTACH_DATA_, \*** **PR_BODY.** Все другие свойства передаваемых сообщений включены в поток TNEF.
  
Следующие предложения предназначены для предоставления списка параметров, которые реализация может решить, как поддерживать:
  
- Следует ли кодировать с помощью MIME или uuencode для исходящие сообщения: boolean.
    
- Набор символов для исходящие сообщения: строка (скопированная непосредственно на параметр charset) или переустановка (переведенная внутренне на строку charset).
    

