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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке в объекте формы. 
  
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
  
> [out] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Для _параметра lppMAPIError_ можно установить NULL, если форма не может предоставить соответствующие сведения для структуры **MAPIERROR.** 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а поставщик адресной книги не поддерживает Юникод, либо MAPI_UNICODE не установлен, а поставщик адресной книги поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Объекты форм реализуют метод **IPersistMessage::GetLastError** для получения сведений о предыдущем вызове метода, который не удалось выполнить. Посетители форм могут предоставить своим пользователям подробные сведения об ошибке, включив данные из структуры [MAPIERROR](mapierror.md) в диалоговое окно. 
  
Вызов **GetLastError** не влияет на состояние формы. При **возвращении GetLastError** форма остается в состоянии, в которое она была до вызова. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать структуру **MAPIERROR,** если форма указывает на нее, на которую указывает параметр  _lppMAPIError,_ только если **GetLastError** возвращает S_OK. Иногда форма не может определить, какая была последняя ошибка, или больше не имеет для отчета об ошибке. В этой ситуации форма возвращает указатель на NULL в _lppMAPIError._ 
  
Дополнительные сведения о **методе GetLastError** см. в расширенных [ошибках MAPI.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

