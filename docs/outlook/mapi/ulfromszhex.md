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
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433054"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Преобразует строку из гексадецимальных цифр null-terminated в незавернутую длинную цепочку. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>Parameters

 _lpsz_
  
> [in] Указатель на завершаемую строку null, которая должна быть преобразована. Параметр  _lpsz_ не должен превышать 65536 символов. 
    
## <a name="return-value"></a>Возвращаемое значение

 **UlFromSzHex** возвращает незаверяемую длинную вставку. Если строка не начинается с хотя бы одной гексадецимальной цифры, возвращается ноль. 
  
## <a name="remarks"></a>Примечания

Функция **UlFromSzHex** перестает преобразовываться, когда достигает первого символа в строке, которая не является гексадецимальной цифрой. Например, с учетом строки "5a" **UlFromSzHex** возвращает значение 90. С учетом строки "5g5h" функция возвращает значение 5. Учитывая строку "g5h5", **UlFromSzHex** возвращает ноль. 
  
 **UlFromSzHex** чувствителен к диакритичным различиям, но позволяет как "a" через "f", так и "A" через "F" для гексадецимальных цифр. Поддерживаются строки в форматах Unicode и DBCS. Ограничение длины  _lpsz имеет_ символы, а не обязательно bytes. 
  

