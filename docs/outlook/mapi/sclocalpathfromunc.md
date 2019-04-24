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
ms.openlocfilehash: e7607a57da5b618a20d6c8e360c7e3cb4f933856
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351249"
---
# <a name="sclocalpathfromunc"></a>ScLocalPathFromUNC

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет путь к локальному пути к указанному UNC-пути. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScLocalPathFromUNC(
  LPSTR szUNC,
  LPSTR szLocal,
  UINT cchLocal
);
```

## <a name="parameters"></a>Параметры

 _Сзунк_
  
> возврата Путь в \\формате [ _Server_]\[ _Share_\[ ] _путь_] файла или каталога.
    
 _Сзлокал_
  
> вышли Путь в формате [ _диск:_]\[ _путь_] того же файла или каталога, что и для параметра _сзунк_ . 
    
 _Кчлокал_
  
> возврата Размер буфера для выходной строки.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Локальный путь успешно найден.
    
МАПИ_Е_ТУ_БИГ
  
>  _сзлокал_ недостаточно велик для хранения результата. 
    
S_FALSE
  
> Строка UNC уже является локальным путем.
    
МАПИ_Е_НОТ_ФАУНД
  
> Локальный путь не найден.
    
## <a name="see-also"></a>См. также



[ScUNCFromLocalPath](scuncfromlocalpath.md)

