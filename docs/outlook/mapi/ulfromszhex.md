---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e6de4be29811dafaf5288b2ccb39c0342a314bad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584627"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Преобразует строку символом null шестнадцатеричных цифр в длинное целое без знака. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>Параметры

 _lpsz_
  
> [in] Указатель на строку символом null, которую нужно преобразовать. Параметр _lpsz_ не должен превышать 65536 символов. 
    
## <a name="return-value"></a>Возвращаемое значение

 **UlFromSzHex** Возвращает длинное целое. Если строка не начинается с по крайней мере один шестнадцатеричных цифр, возвращается значение 0. 
  
## <a name="remarks"></a>Замечания

Функция **UlFromSzHex** прекращает преобразование при достижении первым символом в строке, которая не является шестнадцатеричных цифр. Например **UlFromSzHex** данной строки «5a», возвращает целое значение 90. Учитывая строка «5g5h», функция возвращает целое значение 5. Учитывая строка «g5h5», **UlFromSzHex** возвращает нуль. 
  
 **UlFromSzHex** учета диакритических различия, но обеспечивает как «» до «f» и «» до «F» для шестнадцатеричных цифр. Поддерживаются строки в формате Юникод и DBCS. Ограничение длины на _lpsz_ находится в символы, не обязательно в байтах. 
  

