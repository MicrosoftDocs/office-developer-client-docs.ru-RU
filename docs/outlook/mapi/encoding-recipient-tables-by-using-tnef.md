---
title: Кодив таблицы получателей с помощью TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417961"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Кодив таблицы получателей с помощью TNEF

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Кодив таблицу получателей в потоке TNEF, редко требуется, так как большинство систем обмена сообщениями поддерживают списки получателей напрямую. Как правило, свойства получателя передаются в заголке сообщения. Если необходимо включить таблицу получателей, TNEF может закодировать таблицу получателей как часть обычной обработки. Это делается на начальном этапе обработки TNEF. Поставщик транспорта может включить таблицу получателей сообщения, вызывая метод [ITnef::AddProps](itnef-addprops.md) со свойством **PR_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients),](pidtagmessagerecipients-canonical-property.md)указанным в списке включения. TNEF получает таблицу получателей из сообщения, запрашивает набор столбцов и обрабатывает каждую строку таблицы в потоке TNEF.
  
Альтернативный метод доступен, если поставщику транспорта необходимо изменить таблицу получателей перед ее кодированием. Поставщик транспорта может создать необходимую таблицу и вызвать метод [ITnef::EncodeRecips.](itnef-encoderecips.md) Если в параметре _lpRecipTable_ передается NULL, таблица получателей будет взята непосредственно из сообщения, как описано для **ITnef::AddProps.**
  

