---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435224"
---
# <a name="szfindsz"></a>SzFindSz

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Находит первый вхождение подстроки с завершенным нулом в строке с нулью. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a>Параметры

 _lpsz_
  
> [in] Указатель на строку, о конце null для поиска. Параметр  _lpsz_ не должен превышать 65536 символов. 
    
 _lpszKey_
  
> [in] Указатель на подстроку, одернутую нулом, для поиска. Параметр  _lpszKey не должен_ превышать 65536 символов. 
    
## <a name="return-value"></a>Возвращаемое значение

 **SzFindSz** возвращает указатель на первый символ первого вхождения подстроки в строке. Если подстрока не возникает ни в одной строке, если  _lpszKey_ больше  _lpsz,_ или если любой из параметров имеет значение NULL, возвращается значение NULL. 
  
## <a name="remarks"></a>Примечания

Функция **SzFindSz** ищет только точное совпадение; он чувствителен к различиям в диакритических и диакритических диакритах. Поиск в форматах Юникод и DBCS поддерживается. Ограничение длины для обоих параметров — в символах, а не вбайтах. 
  

