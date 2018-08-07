---
title: Таблицы папок получения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5f3bcda3beb29fa91629ea1639522ef24dc6eb32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812101"
---
# <a name="receive-folder-tables"></a>Таблицы папок получения

  
  
**Относится к**: Outlook 
  
Таблица получения папка содержит сведения для всех папок, обозначены как получения папки для хранения сообщений. Папка получения является там, где размещены входящих сообщений класса определенного сообщения. Реализация поставщиков хранилища сообщений принимать папки таблиц и их использовать клиентские приложения путем вызова метода [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Следующие свойства составляющих обязательный столбец, задайте получают таблиц папки:
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

