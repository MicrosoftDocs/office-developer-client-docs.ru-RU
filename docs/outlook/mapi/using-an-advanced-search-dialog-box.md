---
title: Использование диалогового окна "Расширенный Поиск"
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
# <a name="using-an-advanced-search-dialog-box"></a>Использование диалогового окна "Расширенный Поиск"

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Некоторые контейнеры адресных книг поддерживают функцию расширенного поиска, позволяющую клиентам выполнять поиск по свойствам, отличным от **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Контейнеры адресных книг, поддерживающие Расширенный поиск, имеют свойство объекта Container с именем **пр_сеарч** ([PidTagSearch](pidtagsearch-canonical-property.md)). Этот объект Container предоставляет доступ к таблице отображения, в которой описывается диалоговое окно поиска — диалоговое окно, используемое для ввода и редактирования расширенных критериев поиска.
  
 **Выполнение расширенного поиска в контейнере адресной книги**
  
1. ВыЗовите метод контейнера [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , указав **пр_сеарч** для тега Property и иид_имапиконтаинер для идентификатора интерфейса. 
    
2. ВыЗовите метод **IMAPIProp:: опенпроперти** объекта Search, указав **пр_детаилс_табле** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) для тега свойства и иид_имапитабле для идентификатора интерфейса. 
    
3. ВыЗовите метод [IMAPIProp:: SetProps](imapiprop-setprops.md) объекта Search для установки значений свойств, которые будут использоваться в расширенном поиске. 
    
4. ВыЗовите метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) объекта Search для сохранения расширенных критериев поиска. 
    
Эта последовательность вызовов приводит к ограничению, которое доступно, когда клиент вызывает метод **жетсеарчкритериа** объекта поиска. 
  

