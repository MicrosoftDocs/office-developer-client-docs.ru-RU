---
title: ScLocalPathFromUNC
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScLocalPathFromUNC
api_type:
- COM
ms.assetid: ef5eb5c6-251e-4a3a-8855-7c28804a29ab
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e94692ac4eb401109fcb522e6224c8748bef37f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812210"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**Относится к**: Outlook 
  
Находит аналог локальный путь для указанного универсальных имен пути (UNC). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a>Параметры

 _szUNC_
  
> [in] Путь в формате \\[ _сервер_]\[ _совместное использование_]\[ _путь_] файла или папки.
    
 _szLocal_
  
> [out] Путь в формате [ _диск:_]\[ _путь_] одного файла или папки и для параметра _szUNC_ . 
    
 _cchLocal_
  
> [in] Размер буфера для вывода строки.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Локальный путь был найден.
    
MAPI_E_TOO_BIG
  
>  _szLocal_ не достаточно для хранения результатов. 
    
S_FALSE
  
> Строка UNC уже локальный путь.
    
MAPI_E_NOT_FOUND
  
> Локальный путь не найден.
    
## <a name="see-also"></a>См. также



[ScUNCFromLocalPath](scuncfromlocalpath.md)

