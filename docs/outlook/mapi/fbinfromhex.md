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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414937"
---
# <a name="fbinfromhex"></a>FBinFromHex

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Преобразует строковую репрезентацию гексадецимального номера в двоичные данные. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
BOOL FBinFromHex(
  LPSTR sz,
  LPBYTE pb
);
```

## <a name="parameters"></a>Parameters

 _sz_
  
> [in] Указатель на строку ASCII, завершаемую null-terminated, которая должна быть преобразована. Это не строка Unicode. Допустимые символы включают гексадецимальные символы с нуля до девяти, а также символы верхнего и нижнего регистров A через F.
    
 _pb_
  
> [вышел] Указатель на возвращенный двоичный номер.
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Строка успешно преобразована в двоичный номер. 
    
FALSE 
  
> Строка ввода содержит недействительные гексадецимальные символы ASCII.
    
## <a name="see-also"></a>См. также



[ScBinFromHexBounded](scbinfromhexbounded.md)

