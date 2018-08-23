---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7513e361f4c1c1bcc93cc420f3a1987e0d817c54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580504"
---
# <a name="ufromsz"></a>UFromSz

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Преобразует строку символом null из десятичных цифр в целое число без знака. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Параметры

 _lpsz_
  
> [in] Указатель на строку символом null, которую нужно преобразовать. Параметр _lpsz_ не должен превышать 65536 символов. 
    
## <a name="return-value"></a>������������ ��������

 **UFromSz** возвращает целое число без знака. Если строка не начинается с по крайней мере один десятичное число, возвращается значение 0. 
  
## <a name="remarks"></a>Замечания

Функция **UFromSz** прекращает преобразование при достижении первым символом в строке, которая не является десятичных цифр. Например **UFromSz** данной строки «55», возвращает целое значение 55. Учитывая строка «5a5b», функция возвращает целое значение 5. Учитывая строка «a5b5», **UFromSz** возвращает нуль. 
  
 **UFromSz** учета диакритических различия. Поддерживаются строки в формате Юникод и DBCS. Ограничение длины на _lpsz_ находится в символы, не обязательно в байтах. 
  

