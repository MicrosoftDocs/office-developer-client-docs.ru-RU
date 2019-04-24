---
title: FBinFromHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBinFromHex
api_type:
- COM
ms.assetid: 47e6c576-bd99-4410-8e41-7dd3159b23b7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 55c7deec9d29ae22a07b2f5ccd1c832d56782c03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341645"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Преобразует строковое представление шестнадцатеричного числа в двоичные данные. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Параметры

 _СЗ_
  
> возврата Указатель на строку ASCII с завершающим нулем для преобразования. Он не является строкой Юникода. Допустимые символы включают в себя шестнадцатеричные символы от нуля до девяти, прописные и строчные буквы от A до F.
    
 _pb_
  
> вышли Указатель на возвращаемое двоичное число.
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Строка успешно преобразована в двоичное число. 
    
FALSE 
  
> Входная строка содержит недопустимые шестнадцатеричные символы ASCII.
    
## <a name="see-also"></a>См. также



[ScBinFromHexBounded](scbinfromhexbounded.md)

