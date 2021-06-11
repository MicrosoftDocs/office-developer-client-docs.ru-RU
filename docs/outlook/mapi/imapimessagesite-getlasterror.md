---
title: IMAPIMessageSiteGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetLastError
api_type:
- COM
ms.assetid: 7ea282d7-388a-4f05-9780-f8dbc5c5d395
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cc4de8aa21d4b3b27bf757389b663ebeff69a9cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420740"
---
# <a name="imapimessagesitegetlasterror"></a>IMAPIMessageSite::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, произошедшей в объекте сайта сообщений. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] HRESULT, содержащий значение ошибки, сгенерированное в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая типом возвращенных строк. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI. 
    
 _lppMAPIError_
  
> [вышел] Указатель на указатель на возвращенную структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Этот параметр можно установить в NULL, если нет **структуры MAPIERROR** для возврата. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH
  
> Либо был MAPI_UNICODE флаг и **GetLastError** не поддерживает Unicode, либо MAPI_UNICODE не был установлен, **а GetLastError** поддерживает только Юникод. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPIMessageSite::GetLastError** поставляет сведения о сбойного вызова предыдущего метода. Звонители могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете использовать структуру **MAPIERROR,** на что указывает параметр  _lppMAPIError,_ если MAPI поставляет один только в том случае, если **GetLastError** возвращает S_OK. Иногда MAPI не может определить, что была последняя ошибка, или не имеет ничего больше, чтобы сообщить об ошибке. В этой ситуации вместо указателя на NULL возвращается _в lppMAPIError._ 
  
Дополнительные сведения о **методе GetLastError** см. в рубрике [Использование расширенных ошибок.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)

