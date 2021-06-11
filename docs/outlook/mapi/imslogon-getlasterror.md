---
title: IMSLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.GetLastError
api_type:
- COM
ms.assetid: 3e296f6d-4833-4c68-9b84-df0b09878474
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 472502d0f033370b06a69596944350152ab794f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425878"
---
# <a name="imslogongetlasterror"></a>IMSLogon::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о последней ошибке, которая произошла для объекта магазина сообщений. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] Тип данных HRESULT, содержащий значение ошибки, сгенерированное в предыдущем вызове метода для объекта хранения сообщений.
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая типом возвращенных строк. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI. 
    
 _lppMAPIError_
  
> [вышел] Указатель на указатель на возвращенную структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Параметр _lppMAPIError может_ быть задан в NULL, если не будет **возвращен MAPIERROR.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Используйте **метод IMSLogon::GetLastError** для получения сведений, отображающихся в сообщении пользователю о последней ошибке, возвращаемой из вызова метода для объекта магазина сообщений. 
  
Чтобы освободить всю память, выделенную MAPI для возвращенной структуры **MAPIERROR,** клиентские приложения должны вызывать только функцию [MAPIFreeBuffer.](mapifreebuffer.md) 
  
Возвращаемая стоимость **getLastError** должна быть S_OK для приложения для использования **MAPIERROR.** Даже если возвращаемая S_OK, **MAPIERROR** может не быть возвращена. Если реализация не может определить последнюю ошибку или если **mapIERROR** недоступна для этой ошибки, **GetLastError** возвращает указатель nULL в  _lppMAPIError_ вместо этого. 
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

