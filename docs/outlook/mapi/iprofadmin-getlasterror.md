---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b6964ecde3a78bd1e9ce0ae1dcab0342c5a21a03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430775"
---
# <a name="iprofadmingetlasterror"></a>IProfAdmin::GetLastError

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, которая произошла в объекте администрирования профиля. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _hResult_
  
> [in] Тип данных HRESULT, содержащий значение ошибки, сгенерированное в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом возвращаемой строки. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре [MAPIERROR,](mapierror.md) возвращаемой в  _параметре lppMAPIError,_ имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Для _параметра lppMAPIError_ можно установить NULL, если не существует возвращаемой структуры **MAPIERROR.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен и реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, и реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IProfAdmin::GetLastError** извлекает сведения о последней ошибке, возвращенной при вызове метода для объекта администрирования профиля. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать структуру **MAPIERROR,** если MAPI передает ее, на нее указывает параметр  _lppMAPIError,_ только если **GetLastError** возвращает S_OK. Иногда MAPI не может определить, какая была последняя ошибка, или больше не нужно сообщать об ошибке. В этой ситуации указатель на NULL возвращается _в lppMAPIError._ 
  
Чтобы освободить всю память, выделенную MAPI для структуры **MAPIERROR,** вызовите функцию [MAPIFreeBuffer.](mapifreebuffer.md) 
  
Дополнительные сведения о **методе GetLastError** см. в дополнительных [сведениях об использовании расширенных ошибок.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

