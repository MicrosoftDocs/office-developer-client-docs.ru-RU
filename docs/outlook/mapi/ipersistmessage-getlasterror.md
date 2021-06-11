---
title: IPersistMessageGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2189a39e115236e6c2ec9de8a263ce3982d8b8e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426711"
---
# <a name="ipersistmessagegetlasterror"></a>IPersistMessage::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке в объекте формы. 
  
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
  
> Строки в структуре [MAPIERROR,](mapierror.md) возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI. 
    
 _lppMAPIError_
  
> [вышел] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Параметр _lppMAPIError можно_ установить в NULL, если форма не может предоставить соответствующую информацию для **структуры MAPIERROR.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а поставщик адресной книги не поддерживает Unicode, либо MAPI_UNICODE не был установлен, а поставщик адресной книги поддерживает только Unicode.
    
## <a name="remarks"></a>Примечания

Объекты формы реализуют **метод IPersistMessage::GetLastError,** чтобы предоставить сведения о сбойном вызове предыдущего метода. Зрители форм могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры [MAPIERROR](mapierror.md) в диалоговое окно. 
  
Вызов **GetLastError** не влияет на состояние формы. Когда **GetLastError** возвращается, форма остается в состоянии, в которое она была до вызова. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать структуру **MAPIERROR,** если форма поставляет ее, которая указывается параметром  _lppMAPIError_ только в том случае, если **GetLastError** возвращает S_OK. Иногда форма не может определить, какая последняя ошибка была или больше не имеет ничего, чтобы сообщить об ошибке. В этой ситуации форма возвращает указатель на NULL в  _lppMAPIError_ вместо этого. 
  
Дополнительные сведения о **методе GetLastError** см. в дополнительных сведениях [о расширенных ошибках MAPI.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

