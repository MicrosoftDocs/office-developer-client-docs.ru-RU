---
title: Кодирование таблиц получателей с помощью TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8110eff9b38c76023621f34396d65714a4316d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808391"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>Кодирование таблиц получателей с помощью TNEF

  
  
**Относится к**: Outlook 
  
Кодирования таблице получателей в поток TNEF редко, так как систем обмена сообщениями наиболее поддерживает получателей списки непосредственно. В общем случае свойствами получателя передаются в заголовке сообщения. При необходимости включения получателей таблицы TNEF можно закодировать таблицы получателей в рамках обычного обработки. Для этого на начальном этапе обработки TNEF. Путем вызова метода [ITnef::AddProps](itnef-addprops.md) со свойством **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)), указанный в списке включения поставщика транспорта может включать таблицы получателя сообщения. Формат TNEF получает таблицы получателя из сообщения, запрашивает набор столбцов и обрабатывает каждой строки в таблице в поток TNEF.
  
Следующий метод доступен, если поставщик транспорта должен изменить получателя таблицы перед кодированием. Поставщика транспорта можно создать необходимые таблицы и затем вызвать метод [ITnef::EncodeRecips](itnef-encoderecips.md) . Если NULL передается в параметре _lpRecipTable_ , таблицы получателя берется непосредственно из сообщения, как описано для **ITnef::AddProps**.
  

