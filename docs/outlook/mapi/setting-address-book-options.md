---
title: Установка параметров адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c64f84da6bece809176bf67985b6f55ce92414a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812266"
---
# <a name="setting-address-book-options"></a>Установка параметров адресной книги

  
  
**Относится к**: Outlook 
  
Можно задать три свойства, описывающие параметры для использования в адресной книге:
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    Свойство **PR_AB_SEARCH_PATH** используется [IAddrBook::ResolveName](iaddrbook-resolvename.md) для определения контейнеров для принимать участие в том порядке, в том, что они должны принимать участие и разрешения имен. Для каждого контейнера в **PR_AB_SEARCH_PATH** **IAddrBook::ResolveName** вызывает метод [IABContainer::ResolveNames](iabcontainer-resolvenames.md) . Контейнеры в начале **PR_AB_SEARCH_PATH** выполняется перед контейнеров в конце **PR_AB_SEARCH_PATH**. 
    
    Порядок поиска в **PR_AB_SEARCH_PATH** задается с помощью структуру [SRowSet](srowset.md) ту же структуру, которая используется для представления строки в таблице. Можно просмотреть текущий путь поиска путем вызова метода [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) и измените его путем вызова метода [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md) . 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    Свойство **PR_AB_DEFAULT_DIR** — это идентификатор операции контейнер адресной книги для отображения изначально при отображении в адресной книге. Каталог по умолчанию действует, пока не будет изменено путем вызова метода [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) . Можно просматривать каталог по умолчанию путем вызова метода [IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md) . 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Эти три свойства являются особыми, так как он не может работать с ними с помощью стандартных способов **IMAPIProp** . Вместо этого необходимо использовать методы **IAddrBook** . Так как ни один из этих свойств можно изменить с помощью **IMAPIProp::SetProps**, нет необходимости для вызова **IMAPIProp::SaveChanges** вносить изменения постоянной. Изменения, сделанные через методы **IAddrBook** вступили в силу немедленно. 
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

