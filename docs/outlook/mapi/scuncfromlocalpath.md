---
title: ScUNCFromLocalPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScUNCFromLocalPath
api_type:
- COM
ms.assetid: cc4abf1a-c08c-4462-9d7c-6af506dc07c9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: faba91d813d27f7ea45e978724ce0d4707803cba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590108"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Находит универсальных имен соглашение (UNC) путь эквивалента данного локальный путь.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>Параметры

 _szLocal_
  
> [in] Путь в формате [ _диск:_]\[ _путь_] файла или папки.
    
 _szUNC_
  
> [out] Путь в формате \\[ _сервер_]\[ _совместное использование_]\[ _путь_] одного файла или папки и для параметра _szLocal_ . 
    
 _cchUNC_
  
> [in] Размер буфера для вывода строки.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Аналог путь UNC был найден.
    
MAPI_E_INVALID_PARAMETER
  
> Один или несколько параметров являются недопустимыми.
    
MAPI_E_TOO_BIG
  
>  _szUNC_ не достаточно для хранения результатов. 
    
S_FALSE
  
> Локальный путь уже была строка UNC.
    
## <a name="see-also"></a>См. также



[ScLocalPathFromUNC](sclocalpathfromunc.md)

