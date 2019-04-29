---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429490"
---
# <a name="fpropexists"></a>FPropExists

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Ищет заданный тег свойства в интерфейсе [IMAPIProp](imapipropiunknown.md) или интерфейсе, производном от **IMAPIProp**, например [iMessage](imessageimapiprop.md) или [IMAPIFolder](imapifolderimapicontainer.md). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Параметры

 _побж_
  
> возврата Указатель на интерфейс или интерфейс **IMAPIProp** , производный от **IMAPIProp** , в котором нужно найти тег свойства. 
    
 _Улпроптаг_
  
> возврата Тег свойства для поиска.
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Обнаружено сравнение С указанным тегом свойства. 
    
FALSE 
  
> Не найдено сравнение для данного тега свойства.
    
## <a name="remarks"></a>Примечания

Если тег свойства в параметре _улпроптаг_ имеет тип пт_унспеЦифиед, функция **фпропексистс** ищет для поиска значение только на основе идентификатора свойства. В противном случае сравнение выполняется для всего тега свойства, включая тип. 
  

