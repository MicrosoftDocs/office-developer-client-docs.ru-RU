---
title: Получение таблиц папок
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5ff1a5e3-5b96-4f08-9b9b-aeb14304b23b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417352"
---
# <a name="receive-folder-tables"></a>Получение таблиц папок

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Таблица папки получения содержит сведения для всех папок, назначенных в качестве папки получения для магазина сообщений. Папка получения — это папка, в которой размещаются входящие сообщения определенного класса сообщений. Поставщики магазинов сообщений реализуют таблицы приемных папок, а клиентские приложения используют их, звоня по [методу IMsgStore::GetReceiveFolderTable.](imsgstore-getreceivefoldertable.md) 
  
Следующие свойства составляют необходимый столбец, установленный в таблицах приемных папок:
  
 **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md) 
  
 **PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md) 
  
 **PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

