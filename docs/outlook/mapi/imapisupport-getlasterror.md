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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке объекта поддержки. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _hResult_
  
> [in] Handle to the error value generated in the previous method call for the support object.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом возвращаемой строки. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Для  _параметра lppMAPIError_ можно установить NULL, если не удается получить структуру **MAPIERROR** с соответствующими сведениями об ошибке. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а MAPI не поддерживает Юникод, либо MAPI_UNICODE не установлен, а MAPI поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::GetLastError** реализован для всех объектов поддержки. Вызыватели могут предоставить своим пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете использовать указатель на структуру **MAPIERROR,** если MAPI передает его в параметр  _lppMAPIError,_ только если **GetLastError** возвращает S_OK. Иногда MAPI не может определить, какая была последняя ошибка, или больше не нужно сообщать об ошибке. В этой ситуации  _lppMAPIError_ возвращает указатель на NULL. 
  
Дополнительные сведения о **методе GetLastError** см. в расширенных [ошибках MAPI.](mapi-extended-errors.md)
  
Чтобы освободить всю память, выделенную MAPI, вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) для возвращенной структуры **MAPIERROR.** 
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Расширенные ошибки MAPI](mapi-extended-errors.md)

