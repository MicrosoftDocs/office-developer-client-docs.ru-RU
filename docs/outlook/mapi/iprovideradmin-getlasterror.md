---
title: IProviderAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.GetLastError
api_type:
- COM
ms.assetid: 853ddee5-24d6-423d-b483-6a07a12de51f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4fc4867d5ca20f8e770afa239b0dffbd8ab1c480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439851"
---
# <a name="iprovideradmingetlasterror"></a>IProviderAdmin::GetLastError

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, которая произошла в объекте администрирования поставщика. 
  
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
  
> Строки в **ПАРАМЕТРе MAPIERROR,** возвращенные в  _параметре lppMAPIError,_ имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на возвращенную структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Для  _параметра lppMAPIError_ можно установить NULL, если **MAPIERROR** не возвращается. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов был успешным и возвратил ожидаемое значение или значения.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а **GetLastError** не поддерживает Юникод, либо MAPI_UNICODE не установлен, а **GetLastError** поддерживает только Юникод. 
    
## <a name="remarks"></a>Примечания

Метод **IProviderAdmin::GetLastError** обеспечивает сведения о вызове предыдущего метода, который не удалось вызвать. Вызыватели могут предоставить своим пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете использовать структуру **MAPIERROR,** если MAPI передает ее, на которую указывает параметр  _lppMAPIError,_ только если **GetLastError** возвращает S_OK. Иногда MAPI не может определить, какая была последняя ошибка, или больше не нужно сообщать об ошибке. В этой ситуации указатель на NULL возвращается _в lppMAPIError._ 
  
Дополнительные сведения о **методе GetLastError** см. в дополнительных [сведениях об использовании расширенных ошибок.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

