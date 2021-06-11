---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 311299b00143667b3f2fb22bd7be6c3a52c7141d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434251"
---
# <a name="iablogongetlasterror"></a>IABLogon::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке поставщика адресной книги. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] Ручка к значению ошибки, сгенерированная в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Битмашка флагов, контролируемая типом возвращенных строк. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI. 
    
 _lppMAPIError_
  
> [вышел] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Параметр  _lppMAPIError можно_ установить в NULL, если поставщик не может предоставить структуре **MAPIERROR** соответствующую информацию. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а поставщик адресной книги не поддерживает Unicode, либо MAPI_UNICODE не был установлен, а поставщик адресной книги поддерживает только Unicode.
    
## <a name="remarks"></a>Примечания

Поставщики адресных книг реализуют **метод GetLastError,** чтобы предоставить сведения о сбойных вызовах предыдущего метода. Звонители могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете использовать структуру **MAPIERROR,** на которую указывает параметр  _lppMAPIError,_ если поставщик адресной книги поставляет эту структуру и только если **GetLastError** возвращает S_OK. Иногда поставщик адресной книги не может определить, какая последняя ошибка была или больше не имеет ничего, чтобы сообщить об ошибке. В этой ситуации поставщик адресных книг возвращает указатель на NULL в _lppMAPIError._ 
  
Дополнительные сведения о **методе GetLastError** см. в дополнительных сведениях [о расширенных ошибках MAPI.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

