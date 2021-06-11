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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
32-битное значение, которое используется для описания ошибки или предупреждения.
  
```cpp
typedef LONG HRESULT;
```

## <a name="remarks"></a>Примечания

Тип **данных HRESULT** такой же, как и [тип данных SCODE.](scode.md) 
  
Значение **HRESULT** состоит из следующих полей: 
  
- 1-битный код, указывающий серьезность, где ноль представляет успех, а 1 — сбой.
    
- 4-битное зарезервированное значение.
    
- 11-битный код, указывающий ответственность за ошибку или предупреждение, также известный как код объекта.
    
- 16-битный код, описывающий ошибку или предупреждение.
    
Большинство методов и функций интерфейса MAPI возвращают **значения HRESULT,** чтобы обеспечить подробное формирование причин. **Значения HRESULT** также широко используются в методах интерфейса OLE. OLE предоставляет несколько макрос для преобразования между **значениями HRESULT** и **SCODE,** другим распространенным типом данных для обработки ошибок. 
  
> [!NOTE]
> В 64-битной MAPI **значение HRESULT** по-прежнему равно 32-битным значениям. 
  
Сведения об использовании значений **HRESULT** в OLE см. в справке к *программисту OLE.* Дополнительные сведения об использовании этих значений в MAPI см. в примере [Обработка](error-handling-in-mapi.md) ошибок и любой из следующих методов интерфейса: 
  
[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIViewAdviseSink::OnPrint](imapiviewadvisesink-onprint.md)
  
## <a name="see-also"></a>См. также



[SCODE](scode.md)


[Типы данных MAPI](mapi-data-types.md)

