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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR,](mapierror.md) которая содержит сведения о предыдущей ошибке. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _hResult_
  
> [in] Handle to the error code generated in the previous method call.
    
 _ulFlags_
  
> [in] Битовая маской флагов, которая указывает формат текста, возвращаемого в структуре **MAPIERROR,** на который указывает _lppMAPIError._ Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки должны быть в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки должны быть в формате ANSI.
    
 _lppMAPIError_
  
> [out] Указатель на указатель на структуру **MAPIERROR,** которая содержит сведения о версии, компоненте и контексте для ошибки. Если возвращаемая информация об ошибке не возвращается, для параметра  _lppMAPIError_ можно установить nULL. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Возвращены сведения об ошибке.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp::GetLastError** обеспечивает сведения о вызове предыдущего метода, который не удалось вызвать. Клиенты могут предоставить своим пользователям подробные сведения об ошибке, включив данные из структуры **MAPIERROR** в диалоговое окно. 
  
Все реализации **GetLastError,** предоставляемые MAPI, являются реализациями ANSI, за исключением [реализации IAddrBook.](iaddrbookimapiprop.md) Метод **GetLastError,** включенный в **IAddrBook,** поддерживает Юникод. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Сведения о реализации этого метода удаленным поставщиком транспорта и сообщения, которые этот метод возвращает, до поставщика транспорта, так как конкретные условия ошибки, которые приводят к различным значениям HRESULT, будут разными для разных поставщиков транспорта.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать структуру **MAPIERROR,** на которая указывает параметр  _lppMAPIError,_ если **GetLastError** указывает одно значение, только если возвращаемая величина S_OK. Иногда **GetLastError не** может определить, какая была последняя ошибка, или больше не имеет каких-либо дополнительных данных для отчета об ошибке. В этой ситуации указатель на NULL возвращается _в lppMAPIError._ 
  
Чтобы освободить память для структуры **MAPIERROR,** вызовите [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
Дополнительные сведения о **методе GetLastError** см. в расширенных [ошибках MAPI.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Расширенные ошибки MAPI](mapi-extended-errors.md)

