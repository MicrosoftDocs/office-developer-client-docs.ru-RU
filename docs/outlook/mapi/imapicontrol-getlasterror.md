---
title: IMAPIControlGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.GetLastError
api_type:
- COM
ms.assetid: 83290b8e-fffc-41c8-a01e-578d130b65c5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 10ac4e33b3f734ec2ce3205aa1897e0418cb563d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421153"
---
# <a name="imapicontrolgetlasterror"></a>IMAPIControl::GetLastError

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке управления кнопкой. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _hResult_
  
> [in] Handle to the error value generated in the previous method call.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом возвращаемой строки. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Для  _параметра lppMAPIError_ можно установить NULL, если поставщик не может предоставить структуру **MAPIERROR** с соответствующей информацией. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Поставщики услуг реализуют метод **IMAPIControl::GetLastError** для получения сведений о предыдущем вызове метода, который не удалось выполнить. MAPI может предоставить пользователям подробные сведения об ошибке, отображая данные из структуры **MAPIERROR** в сообщении или диалоговом окне. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Для каждой ошибки нет необходимости включать сведения в структуру **MAPIERROR.** Определить причину предыдущей ошибки может оказаться невозможно. Если у вас есть информация, S_OK данные и соответствующие данные **в структуре MAPIERROR.** Если сведения недоступны, S_OK и указатель на NULL для параметра _lppMAPIError._ 
  
Дополнительные сведения о **методе GetLastError** см. в расширенных [ошибках MAPI.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

