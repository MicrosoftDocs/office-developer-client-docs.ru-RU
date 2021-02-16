---
title: Настройка параметров адресной книги
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
# <a name="setting-address-book-options"></a>Настройка параметров адресной книги

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Можно настроить три свойства, описывая параметры использования адресной книги:
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath)](pidtagabsearchpath-canonical-property.md)
    
    Свойство **PR_AB_SEARCH_PATH** используется [IAddrBook::ResolveName](iaddrbook-resolvename.md) для определения контейнеров, участвующих в разрешении имен, и порядка их использования. Для каждого контейнера **в PR_AB_SEARCH_PATH** **IAddrBook::ResolveName** вызывает метод [IABContainer::ResolveNames.](iabcontainer-resolvenames.md) Контейнеры в начале **PR_AB_SEARCH_PATH** перед контейнерами в конце **PR_AB_SEARCH_PATH.** 
    
    Порядок поиска в **PR_AB_SEARCH_PATH** задан с помощью структуры [SRowSet,](srowset.md) той же структуры, которая используется для представления строк в таблице. Чтобы просмотреть текущий путь поиска, вы можете вызывать метод [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md) и изменять его, вызывая метод [IAddrBook::SetSearchPath.](iaddrbook-setsearchpath.md) 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    Свойство **PR_AB_DEFAULT_DIR** является идентификатором записи контейнера адресной книги, который будет отображаться изначально при отобраствии адресной книги. Параметр каталога по умолчанию остается в силе, пока вы не измените его, вызывая метод [IAddrBook::SetDefaultDir.](iaddrbook-setdefaultdir.md) Чтобы просмотреть каталог по умолчанию, вы можете вызывать метод [IAddrBook::GetDefaultDir.](iaddrbook-getdefaultdir.md) 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab)](pidtagabdefaultpab-canonical-property.md)
    
Эти три свойства являются специальными, так как с ними невозможно работать с помощью стандартных методов **IMAPIProp.** Вместо этого необходимо использовать методы **IAddrBook.** Так как ни одно из этих свойств не может быть изменено с помощью **IMAPIProp::SetProps,** нет необходимости вызывать **IMAPIProp::SaveChanges,** чтобы внести изменения без изменений. Изменения, внося в методы **IAddrBook, вступает** в силу немедленно. 
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

