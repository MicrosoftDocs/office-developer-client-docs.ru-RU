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
ms.openlocfilehash: b88545ede6275bd834fad5869d972e2860a6c77e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573182"
---
# <a name="receive-folder-tables"></a>Таблицы папок получения

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Таблица получения папка содержит сведения для всех папок, обозначены как получения папки для хранения сообщений. Папка получения является там, где размещены входящих сообщений класса определенного сообщения. Реализация поставщиков хранилища сообщений принимать папки таблиц и их использовать клиентские приложения путем вызова метода [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . 
  
Следующие свойства составляющих обязательный столбец, задайте получают таблиц папки:
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

