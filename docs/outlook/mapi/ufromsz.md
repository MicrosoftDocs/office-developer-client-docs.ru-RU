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
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439011"
---
# <a name="ufromsz"></a>UFromSz

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Преобразует строку десятичных цифр с null-terminated в неподписавую цепочку. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Parameters

 _lpsz_
  
> [in] Указатель на завершаемую строку null, которая должна быть преобразована. Параметр  _lpsz_ не должен превышать 65536 символов. 
    
## <a name="return-value"></a>Возвращаемое значение

 **UFromSz** возвращает незаверяемую ставку. Если строка не начинается с хотя бы одной десятичной цифры, возвращается ноль. 
  
## <a name="remarks"></a>Примечания

Функция **UFromSz** прекращает преобразование, когда достигает первого символа в строке, которая не является десятичной цифрой. Например, с учетом строки "55", **UFromSz** возвращает значение 55. С учетом строки "5a5b" функция возвращает значение 5. Учитывая строку "a5b5", **UFromSz** возвращает ноль. 
  
 **UFromSz чувствителен** к диакритичным различиям. Поддерживаются строки в форматах Unicode и DBCS. Ограничение длины  _lpsz имеет_ символы, а не обязательно bytes. 
  

