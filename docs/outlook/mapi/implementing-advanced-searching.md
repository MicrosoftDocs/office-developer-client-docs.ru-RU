---
title: Реализация расширенного поиска
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0ba9958588c476ae330b0f4a413361e80d54667a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571971"
---
# <a name="implementing-advanced-searching"></a>Реализация расширенного поиска

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Некоторые контейнеров адресной книги поддерживает расширенные возможность поиска, который позволяет клиентам для поиска по свойства не **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Для поддержки расширенного поиска, поставщик должен реализовывать специальный контейнер, доступен через свойство **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) на других контейнеров. **PR_SEARCH** содержит объект контейнера, который предоставляет доступ для отображения таблицы с описанием диалоговое окно для ввода и изменить критерии расширенный поиск. 
  
 **Для поддержки расширенного поиска**
  
1. Определение свойства для каждого из условий поиска.
    
2. В разделе код в метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера, который обрабатывает свойство **PR_SEARCH** : 
    
1. Проверьте, что клиент запрашивает интерфейс **IMAPIContainer** . Если запрашивается несоответствующий интерфейс с ошибкой и возвращают MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Создайте новый объект поиска, который поддерживает интерфейс **IMAPIContainer** . 
    
3. На этом этапе будет вызов метода **IMAPIProp::OpenProperty** поиска контейнера для получения его свойство **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)). Ваш поставщик необходимо задать отображаемое таблицы, обычно с помощью вызова [BuildDisplayTable](builddisplaytable.md), с описанием диалоговое окно Расширенный поиск контейнера.
    
4. MAPI отображает поле поиска, что пользователю требуется ввести соответствующие условиям. После завершения работы пользователя, MAPI вызывает метод [IMAPIProp::SetProps](imapiprop-setprops.md) контейнер для хранения условия поиска. 
    
5. Запрос поиска контейнера содержимое таблицы будет выполнен вызов. Заполните таблицу содержимого со всеми записей в контейнере, соответствующие критериям.
    

