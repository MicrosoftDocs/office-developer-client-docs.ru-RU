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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Некоторые контейнеры адресных книг поддерживают расширенные возможности поиска, которые позволяют  клиентам искать свойства, не PR_DISPLAY_NAME[(PidTagDisplayName).](pidtagdisplayname-canonical-property.md) Чтобы поддерживать расширенный поиск, поставщик должен реализовать специальный контейнер, доступный через **свойство** [PR_SEARCH (PidTagSearch)](pidtagsearch-canonical-property.md)других контейнеров. **PR_SEARCH** контейнерный объект, который предоставляет доступ к таблице отображения, в котором описывается диалоговое окно, используемого для ввода и редактирования расширенных критериев поиска. 
  
 **Поддержка расширенных поисков**
  
1. Определите свойство для каждого из критериев поиска.
    
2. В разделе кода в методе [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) который  обрабатывает свойство PR_SEARCH: 
    
1. Убедитесь, что клиент запрашивает **интерфейс IMAPIContainer.** Если запрашивается неприемлемый интерфейс, сбой и возвращение MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Создайте новый объект поиска, поддерживающем **интерфейс IMAPIContainer.** 
    
3. На этом этапе будет выполнен вызов в метод **IMAPIProp::OpenProperty** для  получения свойства [PR_DETAILS_TABLE (PidTagDetailsTable).](pidtagdetailstable-canonical-property.md) Поставщик должен предоставить таблицу отображения, как правило, с помощью вызова [в BuildDisplayTable,](builddisplaytable.md)которая описывает расширенный диалоговое окно поиска контейнера.
    
4. MAPI отображает диалоговое окно поиска, позволяя пользователю вводить соответствующие критерии. По завершению работы с пользователем MAPI вызывает метод [IMAPIProp::SetProps](imapiprop-setprops.md) контейнера для хранения критериев поиска. 
    
5. Для запроса таблицы содержимого контейнера поиска будет выполнен вызов. Заполнять таблицу содержимого всеми записями в контейнере, которые соответствуют критериям.
    

