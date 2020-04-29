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
  
Вы можете задать три свойства, описывающих параметры использования адресной книги:
  
- **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    Свойство **PR_AB_SEARCH_PATH** используется [IAddrBook:: ресолвенаме](iaddrbook-resolvename.md) для определения контейнеров, участвующих в разрешении имен, и порядка, в котором они должны быть задействованы. Для каждого контейнера в **PR_AB_SEARCH_PATH** **IAddrBook:: ресолвенаме** вызывает его метод [иабконтаинер:: ResolveNames](iabcontainer-resolvenames.md) . Контейнеры в начале **PR_AB_SEARCH_PATH** ищутся перед контейнерами в конце **PR_AB_SEARCH_PATH**. 
    
    Порядок поиска в **PR_AB_SEARCH_PATH** задается с помощью структуры [SRowSet](srowset.md) и той же структуры, которая используется для представления строк в таблице. Вы можете просмотреть текущий путь поиска, вызвав метод [IAddrBook:: жетсеарчпас](iaddrbook-getsearchpath.md) и изменив его, вызвав метод [IAddrBook:: сетсеарчпас](iaddrbook-setsearchpath.md) . 
    
- **PR_AB_DEFAULT_DIR** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    Свойство **PR_AB_DEFAULT_DIR** — это идентификатор записи контейнера адресной книги, который должен отображаться первоначально при отображении адресной книги. Параметры каталога по умолчанию действуют до тех пор, пока вы не измените его, вызвав метод [IAddrBook:: сетдефаултдир](iaddrbook-setdefaultdir.md) . Вы можете просмотреть каталог по умолчанию, вызвав метод [IAddrBook:: жетдефаултдир](iaddrbook-getdefaultdir.md) . 
    
- **PR_AB_DEFAULT_PAB** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Эти три свойства являются особыми, так как вы не можете работать с ними с помощью стандартных методов **IMAPIProp** . Вместо этого необходимо использовать методы **IAddrBook** . Так как ни одно из этих свойств не может быть изменено с помощью **IMAPIProp:: SetProps**, нет необходимости вызывать **IMAPIProp:: SaveChanges** , чтобы сделать изменения постоянными. Изменения, внесенные с помощью методов **IAddrBook** , вступают в силу немедленно. 
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

