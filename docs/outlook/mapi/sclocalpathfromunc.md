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
ms.openlocfilehash: e303361f4f0dd3a08dbb362096d07b8b391a6d97
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594420"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Находит аналог локальный путь для указанного универсальных имен пути (UNC). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
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
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Локальный путь был найден.
    
MAPI_E_TOO_BIG
  
>  _szLocal_ не достаточно для хранения результатов. 
    
S_FALSE
  
> Строка UNC уже локальный путь.
    
MAPI_E_NOT_FOUND
  
> Локальный путь не найден.
    
## <a name="see-also"></a>См. также



[ScUNCFromLocalPath](scuncfromlocalpath.md)

