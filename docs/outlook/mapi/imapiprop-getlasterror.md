---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435833"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает [структуру MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] Ручка кода ошибки, сгенерированная в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Битмашка флагов, которая указывает формат текста, возвращаемого в структуре **MAPIERROR,** указываемого _на lppMAPIError._ Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки должны быть в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки должны быть в формате ANSI.
    
 _lppMAPIError_
  
> [вышел] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Параметр  _lppMAPIError можно_ установить в NULL, если не будет возвращена информация об ошибке. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Информация об ошибке была возвращена.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp::GetLastError** поставляет сведения о предыдущем вызове метода, который не удалось. Клиенты могут предоставить своим пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно. 
  
Все реализации **GetLastError,** предоставляемые MAPI, являются реализацией ANSI, за исключением [реализации IAddrBook.](iaddrbookimapiprop.md) Метод **GetLastError,** включенный в **IAddrBook,** поддерживает Юникод. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Сведения о внедрении этого метода удаленным поставщиком транспорта и о том, какие сообщения возвращает этот метод поставщику транспорта, так как определенные условия ошибок, которые приводят к различным значениям HRESULT, будут разными для различных поставщиков транспорта.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете использовать структуру **MAPIERROR,** на что указывает параметр  _lppMAPIError,_ если **GetLastError** поставляет один, только если значение возврата S_OK. Иногда **GetLastError не** может определить, какая последняя ошибка была или больше не имеет ничего, чтобы сообщить об ошибке. В этой ситуации вместо указателя на NULL возвращается _в lppMAPIError._ 
  
Чтобы освободить память для **структуры MAPIERROR,** позвоните в [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
Дополнительные сведения о **методе GetLastError** см. в дополнительных сведениях [о расширенных ошибках MAPI.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Расширенные ошибки MAPI](mapi-extended-errors.md)

