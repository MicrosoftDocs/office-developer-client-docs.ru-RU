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
ms.openlocfilehash: 67aa5b3d85de3df659b5aa1a351ec0d1dcf90248
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809027"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**Относится к**: Outlook 
  
Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибки. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _hResult_
  
> [in] Дескриптор код ошибки, созданный в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Битовая маска флаги, которое указывает формат для текста, возвращаемых в структуре **MAPIERROR** , на который указывает _lppMAPIError_. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки должны быть в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки должен быть в формате ANSI.
    
 _lppMAPIError_
  
> [out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки. Параметр _lppMAPIError_ может быть присвоено значение NULL, если нет данных об ошибках для возврата. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Возвращает сведения об ошибке.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Замечания

Метод **IMAPIProp::GetLastError** предоставляет сведения о предыдущий вызов, завершившихся сбоем. Клиенты можно предоставить своим пользователям подробные сведения об ошибке, включая данные из структуры **MAPIERROR** в диалоговое окно. 
  
Все реализации **GetLastError** предоставлено MAPI, реализации ANSI, за исключением реализации [IAddrBook](iaddrbookimapiprop.md) . Метод **GetLastError** , включенные в состав **IAddrBook** поддерживает Юникод. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Сведения о удаленной транспорта поставщика реализация этого метода и какие сообщения, этот метод возвращает все периоды до поставщика транспорта, так как условия ошибки, которые привести к различные значения HRESULT будет отличаться для разных транспорта Поставщики.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать структуры **MAPIERROR** , указывает _lppMAPIError_ параметр, если **GetLastError** предоставляет, только в том случае, если возвращаемым значением является значение S_OK. В некоторых случаях **GetLastError** не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит. В этом случае указатель на значение NULL, возвращается в _lppMAPIError_ вместо этого. 
  
Чтобы освободить память для структуры **MAPIERROR** , вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Расширенных ошибки MAPI](mapi-extended-errors.md)

