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
ms.openlocfilehash: 667eda2a018d2a5d712950a31e05ec0ba9bb32ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812226"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Относится к**: Outlook 
  
Находит универсальных имен соглашение (UNC) путь эквивалента данного локальный путь.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Аналог путь UNC был найден.
    
MAPI_E_INVALID_PARAMETER
  
> Один или несколько параметров являются недопустимыми.
    
MAPI_E_TOO_BIG
  
>  _szUNC_ не достаточно для хранения результатов. 
    
S_FALSE
  
> Локальный путь уже была строка UNC.
    
## <a name="see-also"></a>См. также



[ScLocalPathFromUNC](sclocalpathfromunc.md)

