---
title: IMAPIFormMgrGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.GetLastError
api_type:
- COM
ms.assetid: 5d908771-ec16-444d-a9b6-44cc75a4d715
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7aff4ad57fd57b6f49ae0f7b7fd7933e5b814866
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425150"
---
# <a name="imapiformmgrgetlasterror"></a>IMAPIFormMgr::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, порожденной объектом диспетчера форм. 
  
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
  
> Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI. 
    
 _lppMAPIError_
  
> [вышел] Указатель на указатель на возвращенную структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Этот параметр можно установить в NULL, если нет **структуры MAPIERROR** для возврата. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг и **GetLastError** не поддерживает Unicode, либо MAPI_UNICODE не был установлен, **а GetLastError** поддерживает только Юникод. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFormMgr::GetLastError** поставляет сведения о предыдущем вызове метода, который не удалось. Звонители могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать структуру **MAPIERROR,** на что указывает параметр  _lppMAPIError,_ если MAPI поставляет ее только в том случае, если **GetLastError** возвращает S_OK. Иногда MAPI не может определить, какая последняя ошибка была или не имеет ничего больше, чтобы сообщить об ошибке. В этой ситуации NULL возвращается в  _lppMAPIError_ вместо этого. 
  
Дополнительные сведения о **методе GetLastError** см. в рубрике [Использование расширенных ошибок.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

