---
title: Использование диалогового окна "Расширенный поиск"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 581607e184d67413e735c4cbfb874643b3222a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588771"
---
# <a name="using-an-advanced-search-dialog-box"></a>Использование диалогового окна "Расширенный поиск"

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Некоторые контейнеров адресной книги поддерживает расширенные возможность поиска, который позволяет клиентам для поиска по свойства не **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Контейнеры адресной книги, которые поддерживают расширенный поиск имеют свойство объекта контейнера **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Этот объект-контейнер предоставляет доступ для отображения таблицы с описанием диалоговое окно поиска — диалоговое окно используется для ввода и изменить критерии расширенный поиск.
  
 **Для выполнения расширенного поиска на контейнер адресной книги**
  
1. Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера, указав **PR_SEARCH** для свойства tag и IID_IMAPIContainer для идентификатора интерфейса. 
    
2. Вызовите метод **IMAPIProp::OpenProperty** объекта поиска, задание для свойства tag и IID_IMAPITable **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) для идентификатор интерфейса. 
    
3. Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) объект поиска, чтобы установить значения для свойств для использования в расширенный поиск. 
    
4. Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) объект поиска, чтобы сохранить критерии расширенный поиск. 
    
В этом последовательность вызовов приводит к ограничениям, становится доступным, когда клиент вызывает метод **GetSearchCriteria** объекта поиска. 
  

