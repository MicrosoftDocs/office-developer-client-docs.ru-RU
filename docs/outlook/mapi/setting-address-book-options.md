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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351410"
---
# <a name="setting-address-book-options"></a>Настройка параметров адресной книги

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вы можете задать три свойства, описывающих параметры использования адресной книги:
  
- **Пр_аб_сеарч_пас** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md))
    
    Свойство **пр_аб_сеарч_пас** используется [IAddrBook:: ресолвенаме](iaddrbook-resolvename.md) для определения контейнеров, участвующих в разрешении имен, и порядка, в котором они должны быть задействованы. Для каждого контейнера в **пр_аб_сеарч_пас**, **IAddrBook:: Ресолвенаме** вызывает метод [иабконтаинер:: ResolveNames](iabcontainer-resolvenames.md) . Контейнеры в начале **пр_аб_сеарч_пас** ищутся перед контейнерами в конце **пр_аб_сеарч_пас**. 
    
    Порядок поиска в **пр_аб_сеарч_пас** указывается с помощью структуры [SRowSet](srowset.md) , той же структуры, которая используется для представления строк в таблице. Вы можете просмотреть текущий путь поиска, вызвав метод [IAddrBook:: жетсеарчпас](iaddrbook-getsearchpath.md) и изменив его, вызвав метод [IAddrBook:: сетсеарчпас](iaddrbook-setsearchpath.md) . 
    
- **Пр_аб_дефаулт_дир** ([PidTagAbDefaultDir](pidtagabdefaultdir-canonical-property.md))
    
    Свойство **пр_аб_дефаулт_дир** — это идентификатор записи контейнера адресной книги, который будет отображаться первоначально при отображении адресной книги. Параметры каталога по умолчанию действуют до тех пор, пока вы не измените его, вызвав метод [IAddrBook:: сетдефаултдир](iaddrbook-setdefaultdir.md) . Вы можете просмотреть каталог по умолчанию, вызвав метод [IAddrBook:: жетдефаултдир](iaddrbook-getdefaultdir.md) . 
    
- **Пр_аб_дефаулт_паб** ([PidTagAbDefaultPab](pidtagabdefaultpab-canonical-property.md))
    
Эти три свойства являются особыми, так как вы не можете работать с ними с помощью стандартных методов **IMAPIProp** . Вместо этого необходимо использовать методы **IAddrBook** . Так как ни одно из этих свойств не может быть изменено с помощью **IMAPIProp:: SetProps**, нет необходимости вызывать **IMAPIProp:: SaveChanges** , чтобы сделать изменения постоянными. Изменения, внесенные с помощью методов **IAddrBook** , вступают в силу немедленно. 
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

