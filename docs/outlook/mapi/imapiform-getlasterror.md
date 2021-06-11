---
title: IMAPIFormGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetLastError
api_type:
- COM
ms.assetid: 81af8a0b-4ec2-459c-8ab2-29d28a8b680f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a74ad733b91aa455b8e03e6aac8efa2c4299b640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426907"
---
# <a name="imapiformgetlasterror"></a>IMAPIForm::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, сгенерированной объектом формы. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] Тип данных HRESULT, содержащий значение ошибки, сгенерированное в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая типом возвращенных строк. Можно установить следующий флаг: 
    
MAPI_UNICODE 
  
> Если установлено, строки в структуре **MAPIERROR,** возвращенные в  _параметре lppMAPIError,_ находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI. 
    
 _lppMAPIError_
  
> [вышел] Указатель на указатель на возвращенную структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Этот параметр можно установить в NULL, если нет **структуры MAPIERROR** для возврата. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг и **GetLastError** не поддерживает Unicode, либо MAPI_UNICODE не был установлен, **а GetLastError** поддерживает только Юникод. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPIForm::GetLastError** поставляет сведения о сбойного вызова предыдущего метода. Звонители могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете использовать структуру **MAPIERROR,** на что указывает параметр  _lppMAPIError,_ если MAPI поставляет один, только если **GetLastError** возвращает S_OK. Иногда MAPI не может определить, какая была последняя ошибка, или она не имеет ничего больше, чтобы сообщить об ошибке. В этой ситуации вместо указателя на NULL возвращается _в lppMAPIError._ 
  
Дополнительные сведения о **методе GetLastError** см. в рубрике [Использование расширенных ошибок.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

