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
ms.openlocfilehash: 3426fd29090a6ab1bb0e66f9bb746e84abe3a25e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589450"
---
# <a name="imapimessagesitegetlasterror"></a>IMAPIMessageSite::GetLastError

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущей появление сообщения объект сайта. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _hResult_
  
> [in] HRESULT, который содержит значение ошибки, созданный в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип возвращаемой строки. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на структуру возвращенные **MAPIERROR** , версии, компонент и контекста сведения об ошибке. Этот параметр может быть присвоено значение NULL, если структура не **MAPIERROR** для возврата. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH
  
> Либо был установлен флажок MAPI_UNICODE и **GetLastError** не поддерживает Юникод, или MAPI_UNICODE не было установлено и **GetLastError** поддерживает только Юникод. 
    
## <a name="remarks"></a>Замечания

Метод **IMAPIMessageSite::GetLastError** предоставляет сведения о предыдущий вызов, завершившихся сбоем. Вызывающие объекты можно предоставить своим пользователям подробные сведения об ошибке, включая данные из структуры **MAPIERROR** в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы использовать **MAPIERROR** структуры, на который указывает с помощью параметра _lppMAPIError_ Если MAPI предоставляет только в том случае, если **код последней ошибки** возвращается значение S_OK. В некоторых случаях MAPI не может определить, что последней ошибкой был или не имеет никакого дополнительно, чтобы сообщить об ошибке. В этом случае указатель на значение NULL, возвращается в _lppMAPIError_ вместо этого. 
  
Дополнительные сведения о методе **GetLastError** отображаются [С помощью расширенных ошибки](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)

