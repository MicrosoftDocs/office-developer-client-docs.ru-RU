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
ms.openlocfilehash: b53dd9aaaf18dba5c7e33e0bc7d984de757634a4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414538"
---
# <a name="scuncfromlocalpath"></a>ScUNCFromLocalPath

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет путь в формате UNC к заданному локальному пути.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
SCODE ScUNCFromLocalPath(
  LPSTR szLocal,
  LPSTR szUNC,
  UINT cchUNC
);
```

## <a name="parameters"></a>Параметры

 _Сзлокал_
  
> возврата Путь в формате [ _диск:_]\[ _путь_] файла или каталога.
    
 _Сзунк_
  
> вышли \\Путь в формате [ _Server_]\[ _Общий_\[ _путь] к_тому же файлу или каталогу, что и для параметра _сзлокал_ . 
    
 _Кчунк_
  
> возврата Размер буфера для выходной строки.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Аналогичный UNC-путь был успешно найден.
    
МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР
  
> Один или несколько параметров являются недопустимыми.
    
МАПИ_Е_ТУ_БИГ
  
>  _сзунк_ недостаточно велик для хранения результата. 
    
S_FALSE
  
> Локальный путь уже является строкой UNC.
    
## <a name="see-also"></a>См. также



[ScLocalPathFromUNC](sclocalpathfromunc.md)

