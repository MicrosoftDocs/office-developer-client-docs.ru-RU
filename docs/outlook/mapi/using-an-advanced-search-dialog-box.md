---
title: Использование диалоговых окна "Расширенный поиск"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c9a156e6-3472-4409-a4ba-3a1a65b7bdcd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 70b62eeaf6e737747c98b3abcd6e7053f71d4308
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437303"
---
# <a name="using-an-advanced-search-dialog-box"></a>Использование диалоговых окна "Расширенный поиск"

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Некоторые контейнеры адресных книг поддерживают расширенный поиск, который позволяет клиентам искать свойства, не PR_DISPLAY_NAME **(** [PidTagDisplayName).](pidtagdisplayname-canonical-property.md) Контейнеры адресной книги, поддерживают расширенный поиск, имеют свойство объекта контейнера **PR_SEARCH** ([PidTagSearch).](pidtagsearch-canonical-property.md) Этот объект контейнера предоставляет доступ к таблице отображения, описываемой диалоговом окне поиска — диалоговом окне, используемом для ввода и изменения расширенных критериев поиска.
  
 **Выполнение расширенных поисков в контейнере адресной книги**
  
1. Вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера,  указав PR_SEARCH для тега свойства и IID_IMAPIContainer для идентификатора интерфейса. 
    
2. Вызовите метод **IMAPIProp::OpenProperty** объекта поиска, указав **PR_DETAILS_TABLE** ([PidTagDetailsTable)](pidtagdetailstable-canonical-property.md)для тега свойства и IID_IMAPITable для идентификатора интерфейса. 
    
3. Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) объекта поиска, чтобы установить значения свойств, которые будут использоваться в расширенных поисковых запросах. 
    
4. Вызовите метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) объекта поиска, чтобы сохранить расширенные условия поиска. 
    
Эта последовательность вызовов приводит к ограничению, когда клиент вызывает метод **GetSearchCriteria** объекта поиска. 
  

