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
ms.openlocfilehash: 64fcbebbd71bc3f478f36c711e49db9a3518ef9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435021"
---
# <a name="hresult"></a>HRESULT

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
32-разрядное значение, используемое для описания ошибки или предупреждения.
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>Примечания

Тип данных **HRESULT** такой же, как и тип данных [SCODE](scode.md) . 
  
Значение **HRESULT** состоит из следующих полей: 
  
- 1 – битовый код, указывающий серьезность, где ноль соответствует успеху, а 1 — ошибка.
    
- 4 зарезервированное значение.
    
- 11 бит кода, указывающий ответственность за сообщение об ошибке или предупреждение, также называемый кодом средства.
    
- 16 – битовый код, описывающий ошибку или предупреждение.
    
Большинство методов и функций интерфейса MAPI возвращают значения **HRESULT** для предоставления детального формирования причин. Значения **HRESULT** также широко используются в методах интерфейса OLE. OLE предоставляет несколько макросов для преобразования между значениями **HRESULT** и значениями **SCODE** , а также другой общий тип данных для обработки ошибок. 
  
> [!NOTE]
> В 64-разрядном MAPI значение **HRESULT** по-прежнему является 32-битным значением. 
  
Сведения об использовании значений **HRESULT** в OLE приведены в статье *Справочник программиста по OLE* . Дополнительные сведения об использовании этих значений в MAPI можно найти в статье [Обработка ошибок](error-handling-in-mapi.md) и любой из следующих методов интерфейса: 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>См. также



[SCODE](scode.md)


[Типы данных MAPI](mapi-data-types.md)

