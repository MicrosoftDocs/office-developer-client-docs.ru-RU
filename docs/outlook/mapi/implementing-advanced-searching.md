---
title: Реализация расширенных поисков
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 08cc60d4-cac8-4ba5-bd7f-a56e63697be3
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 35d41ff903c5ed22c5210adf6448dfded0afe4b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407391"
---
# <a name="implementing-advanced-searching"></a>Реализация расширенных поисков

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Некоторые контейнеры адресной книги поддерживают расширенный поиск, который позволяет клиентам искать свойства, кроме **PR_DISPLAY_NAME** ([PidTagDisplayName).](pidtagdisplayname-canonical-property.md) Для поддержки расширенных поисковых запросов поставщик должен реализовать специальный контейнер, доступный через свойство **PR_SEARCH** ([PidTagSearch)](pidtagsearch-canonical-property.md)других контейнеров. **PR_SEARCH** содержит объект контейнера, который предоставляет доступ к таблице отображения, в котором описывается диалоговое окно, используемого для ввода и изменения расширенных критериев поиска. 
  
 **Поддержка расширенных поисков**
  
1. Определите свойство для каждого условия поиска.
    
2. В разделе кода в методе [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **контейнера,** который обрабатывает PR_SEARCH свойства: 
    
1. Убедитесь, что клиент запрашивает **интерфейс IMAPIContainer.** Если запрашивается недопустимый интерфейс, сбой и возврат MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Создайте новый объект поиска, который поддерживает **интерфейс IMAPIContainer.** 
    
3. На этом этапе будет выполнен вызов метода **IMAPIProp::OpenProperty** контейнера поиска для получения его свойства **PR_DETAILS_TABLE** ([PidTagDetailsTable).](pidtagdetailstable-canonical-property.md) Поставщик должен предоставить отображаемую таблицу, обычно с помощью вызова [BuildDisplayTable,](builddisplaytable.md)которая описывает диалоговое окно "Расширенный поиск" контейнера.
    
4. MAPI отображает диалоговое окно поиска, позволяя пользователю вводить соответствующие условия. Когда пользователь завершит работу, MAPI вызывает метод [контейнера IMAPIProp::SetProps](imapiprop-setprops.md) для хранения критериев поиска. 
    
5. Будет выполнен вызов для запроса таблицы содержимого контейнера поиска. Заполнять таблицу содержимого всеми записями в контейнере, которые соответствуют условиям.
    

