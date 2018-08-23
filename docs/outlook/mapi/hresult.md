---
title: HRESULT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HRESULT
api_type:
- COM
ms.assetid: b248ed11-3d8a-4d4c-9b84-fa5bee7979c7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a3e46732f9b74b9cdf2dc4c961e7b6b66e3d91d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565230"
---
# <a name="hresult"></a>HRESULT

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Значение 32-разрядная версия, используемый для описания сообщение об ошибке или предупреждение.
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>Замечания

Тип данных **HRESULT** — то же, что тип данных [SCODE](scode.md) . 
  
Значение **HRESULT** состоит из следующих полей: 
  
- 1-разрядный код, указывающий уровень серьезности, где нулевой представляет успеха и 1 представляет сбоя.
    
- 4-битное значение зарезервировано.
    
- 11-разрядный код, указывающее ответственность за сообщение об ошибке или предупреждение, также известной как код средства.
    
- 16-разрядный код, описывающее ошибку или предупреждение.
    
Большинство методов интерфейса MAPI и функции, возвращаемые значения **HRESULT** для предоставления подробные причина возникновения. Значения **HRESULT** также получила широкого применения в методы интерфейса OLE. OLE предоставляет несколько макросов для преобразования значения **HRESULT** и значения **SCODE** введите другой общих данных для обработки ошибок. 
  
> [!NOTE]
> В 64-разрядная версия MAPI **HRESULT** по-прежнему значение 32-разрядная версия. 
  
Дополнительные сведения об использовании OLE значения **HRESULT** видеть *OLE Справочник программиста* . Дополнительные сведения об использовании этих значений в MAPI можно [Обработки ошибок](error-handling-in-mapi.md) и какие-либо из следующих методов интерфейса: 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>См. также



[SCODE](scode.md)


[Типы данных MAPI](mapi-data-types.md)

