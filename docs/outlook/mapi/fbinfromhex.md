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
ms.openlocfilehash: 87a470c1c682225eb1deefba9ccc8c12fbdc49c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569829"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Преобразует строковое представление шестнадцатеричного числа в двоичных данных. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Параметры

 _sz_
  
> [in] Указатель на строку ASCII символом null, которую нужно преобразовать. Не является строка Юникода. Допустимые знаки включают шестнадцатеричных знаков нулевой до девяти как, так и прописные и строчные буквы A до F.
    
 _pb_
  
> [out] Указатель на возвращаемый двоичное число.
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Строка была успешно преобразуется в двоичное. 
    
FALSE 
  
> Входная строка содержит недопустимый шестнадцатеричных знаков ASCII.
    
## <a name="see-also"></a>См. также



[ScBinFromHexBounded](scbinfromhexbounded.md)

