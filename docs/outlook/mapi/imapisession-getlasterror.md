---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7477213ee854be1ae71b47a0c1b339c4c13b6f04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435581"
---
# <a name="imapisessiongetlasterror"></a>IMAPISession::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает [структуру MAPIERROR, которая](mapierror.md) содержит сведения об ошибке предыдущего сеанса. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] Ручка к значению ошибки, сгенерированная в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая типом возвращенных строк. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI. 
    
 _lppMAPIError_
  
> [вышел] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Параметр _lppMAPIError можно_ установить в NULL, если MAPI не может предоставить соответствующую информацию для **структуры MAPIERROR.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Флаг MAPI_UNICODE и сеанс не поддерживает Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::GetLastError** извлекает сведения о последней ошибке, которая была возвращена вызовом метода **IMAPISession.** Клиенты могут предоставить своим пользователям подробные сведения об ошибке, включив эти сведения в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете использовать структуру **MAPIERROR,** если MAPI поставляет один, на который указывает параметр  _lppMAPIError,_ только если **GetLastError** возвращает S_OK. Иногда MAPI не может определить, какая была последняя ошибка, или она не имеет ничего больше, чтобы сообщить об ошибке. В этой ситуации **GetLastError** возвращает указатель на NULL в _lppMAPIError._ 
  
Дополнительные сведения о **методе GetLastError** см. в дополнительных сведениях [о расширенных ошибках MAPI.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Расширенные ошибки MAPI](mapi-extended-errors.md)

