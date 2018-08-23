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
ms.openlocfilehash: 3e641842dd8264c0cd3556c498bd74c77bda32f7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577508"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR](mapierror.md) , содержащий сведения об ошибке предыдущей объект поддержки. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _hResult_
  
> [in] Дескриптор значение ошибки, созданный в предыдущем вызове метода для объекта поддержки.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип возвращаемой строки. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки. Параметр _lppMAPIError_ может быть присвоено значение NULL, если структура **MAPIERROR** с сведения об ошибке. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и MAPI не поддерживает Юникод, или MAPI_UNICODE не было установлено и MAPI поддерживает только Юникод.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::GetLastError** применяется для всех объектов поддержки. Вызывающие объекты можно предоставить своим пользователям подробные сведения об ошибке, включая данные из структуры **MAPIERROR** в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Указатель на структуру **MAPIERROR** можно использовать, если MAPI предоставляет один с помощью параметра _lppMAPIError_ только в том случае, если **код последней ошибки** возвращается значение S_OK. В некоторых случаях MAPI не может определить последнюю ошибку был или он не более отчет об ошибке содержит. В этом случае _lppMAPIError_ возвращает указатель на значение NULL вместо этого. 
  
Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).
  
Для освобождения всех памяти, выделенной MAPI, вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) для возвращаемых структуры **MAPIERROR** . 
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Расширенных ошибки MAPI](mapi-extended-errors.md)

