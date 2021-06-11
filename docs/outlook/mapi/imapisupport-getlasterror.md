---
title: IMAPISupportGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c34c175c43ada03e982f08a27f675448ea24a567
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438549"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке объекта поддержки. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] Ручка к значению ошибки, сгенерированная в предыдущем вызове метода для объекта поддержки.
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая типом возвращенных строк. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI. 
    
 _lppMAPIError_
  
> [вышел] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Параметр  _lppMAPIError может_ быть задан в NULL, если структура **MAPIERROR** с соответствующей информацией об ошибке не может быть предоставлена. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов удался и возвращает ожидаемое значение или значения.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а MAPI не поддерживает Unicode, либо MAPI_UNICODE не был установлен, а MAPI поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::GetLastError** реализован для всех объектов поддержки. Звонители могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Указатель можно использовать в структуре **MAPIERROR,** если MAPI поставляет один, в  _параметре lppMAPIError_ только в том случае, если **GetLastError** возвращает S_OK. Иногда MAPI не может определить, что была последняя ошибка или она не имеет ничего больше, чтобы сообщить об ошибке. В этой ситуации  _вместо этого lppMAPIError_ возвращает указатель в NULL. 
  
Дополнительные сведения о **методе GetLastError** см. в дополнительных сведениях [о расширенных ошибках MAPI.](mapi-extended-errors.md)
  
Чтобы освободить всю память, выделенную MAPI, вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) для возвращенной структуры **MAPIERROR.** 
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Расширенные ошибки MAPI](mapi-extended-errors.md)

