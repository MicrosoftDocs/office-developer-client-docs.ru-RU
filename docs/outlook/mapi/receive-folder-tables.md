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
ms.openlocfilehash: b291167a0457eaaf4f3bcb48ab36d6c6e6512fcc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328478"
---
# <a name="receive-folder-tables"></a>Таблицы папок получения

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Таблица получить папку содержит сведения обо всех папках, назначенных в качестве папок получения для хранилища сообщений. Папка получения — это папка, в которой размещаются входящие сообщения определенного класса сообщений. Поставщики хранилищ сообщений реализуют таблицы получения и клиентские приложения используют их, выполнив вызов метода [IMsgStore:: жетрецеивефолдертабле](imsgstore-getreceivefoldertable.md) . 
  
Следующие свойства составляют обязательный набор столбцов в таблицах получения папок:
  
 **Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 
  
 **Пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) 
  
 **Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

