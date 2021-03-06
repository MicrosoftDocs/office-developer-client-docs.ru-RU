---
title: Хранилища сообщений по умолчанию
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1ad325c68241c8a3924909b4dbf42c9657e68352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338047"
---
# <a name="default-message-stores"></a>Хранилища сообщений по умолчанию

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Хранилище сообщений по умолчанию – это хранилище, которое клиентское приложение может использовать в общие целях, обмена сообщениями. Существует ряд дополнительных вариантов поставщиков хранилища сообщений, которые могут потребоваться, если поставщик хранилища сообщений будет использоваться в качестве хранилища сообщений по умолчанию. Это происходит в следующих случаях:
  
- Реализация специальных папок: Входящие, Оправленные и папки результатов поиска.
    
- Предоставление отчетов для чтения и не предназначенных для чтения.
    
- Разрешение на отправки входящих и исходящих сообщений.
    
- Разрешение создания сообщений с произвольными классами сообщений.
    
- Свойства, поддерживающие имена и несколько значений.
    
- Поддержка функции[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md), даже если поставщик хранилища сообщений  тесно связан с поставщиком передачи данных. 
    
- Поддержка таблиц со связанным содержимым. Дополнительные сведения см. в статье [Содержимое таблиц](contents-tables.md).
    
- Поддержка уведомлений программы буферизации MAPI при наличии очереди исходящих сообщений.
    
## <a name="see-also"></a>См. также



[Разработка поставщика хранилища сообщений MAPI](developing-a-mapi-message-store-provider.md)

