---
title: Параметры настройки адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9bd31233-fc8d-4e0a-9f1b-218c5ecb6d1b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f72c916e917543b11089f8f5ef1aa4b9552a1b6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417345"
---
# <a name="setting-address-book-options"></a>Параметры настройки адресной книги

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Можно установить три свойства, описывая варианты использования адресной книги:
  
- **PR_AB_SEARCH_PATH** [(PidTagAbSearchPath)](pidtagabsearchpath-canonical-property.md)
    
    Свойство **PR_AB_SEARCH_PATH** [используется IAddrBook::ResolveName](iaddrbook-resolvename.md) для определения контейнеров, участвующих в разрешении имен, и порядка их участия. Для каждого контейнера **в PR_AB_SEARCH_PATH,** **IAddrBook::ResolveName** вызывает свой [метод IABContainer::ResolveNames.](iabcontainer-resolvenames.md) Контейнеры в начале **PR_AB_SEARCH_PATH** до контейнеров в конце **PR_AB_SEARCH_PATH**. 
    
    Порядок поиска **в PR_AB_SEARCH_PATH** указывается с помощью структуры [SRowSet,](srowset.md) той же структуры, которая используется для представления строк в таблице. Вы можете просмотреть текущий путь поиска, позвонив [методу IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) и измените его, назвав [метод IAddrBook::SetSearchPath.](iaddrbook-setsearchpath.md) 
    
- **PR_AB_DEFAULT_DIR** [(PidTagAbDefaultDir)](pidtagabdefaultdir-canonical-property.md)
    
    Свойство **PR_AB_DEFAULT_DIR** является идентификатором входа контейнера адресной книги, который будет отображаться на начальном этапе при отобраствии адресной книги. Параметр каталога по умолчанию остается в силе до тех пор, пока вы не измените его, назвав [метод IAddrBook::SetDefaultDir.](iaddrbook-setdefaultdir.md) Вы можете просмотреть каталог по умолчанию, позвонив [методу IAddrBook::GetDefaultDir.](iaddrbook-getdefaultdir.md) 
    
- **PR_AB_DEFAULT_PAB** [(PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Эти три свойства являются особыми, так как с ними нельзя работать с помощью стандартных **методов IMAPIProp.** Вместо этого необходимо использовать **методы IAddrBook.** Поскольку ни одно из этих свойств не может быть изменено с **помощью IMAPIProp::SetProps,** нет необходимости вызывать **IMAPIProp::SaveChanges,** чтобы внести изменения навсегда. Изменения, сделанные с помощью **методов IAddrBook,** вступает в силу немедленно. 
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

