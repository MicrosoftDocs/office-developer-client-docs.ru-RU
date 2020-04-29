---
title: ScBinFromHexBounded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScBinFromHexBounded
api_type:
- COM
ms.assetid: edac715c-6edb-4b05-82e5-c08c3c7cb6d4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 813fab28e3e865c9f04f85c854b292ce7229dad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439760"
---
# <a name="scbinfromhexbounded"></a>ScBinFromHexBounded

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Преобразует заданную часть строкового представления шестнадцатеричного числа в двоичное число. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScBinFromHexBounded(
  LPSTR sz,
  LPBYTE pb,
  ULONG cb
);
```

## <a name="parameters"></a>Параметры

 _сз_
  
> возврата Указатель на преобразуемую строку, заканчивающуюся нулем. Допустимыми символами являются шестнадцатеричные символы от 0 до 9, а как прописные, так и строчные буквы от a до f.
    
 _pb_
  
> вышли Указатель на возвращаемое двоичное число.
    
 _cb_
  
> возврата Размер (в байтах) параметра _Pb_ . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Преобразование выполнено успешно.
    
MAPI_E_CALL_FAILED
  
> Обнаружены недопустимые символы.
    
## <a name="see-also"></a>См. также



[FBinFromHex](fbinfromhex.md)

