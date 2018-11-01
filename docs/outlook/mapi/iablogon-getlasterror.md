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
ms.openlocfilehash: 1cd432540a4336b46a589e953b5ce4dde7553597
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573665"
---
# <a name="iablogongetlasterror"></a>IABLogon::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем Ошибка поставщика адресной книги. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _hResult_
  
> [in] Дескриптор значение ошибки, созданный в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип возвращаемой строки. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки. Параметр _lppMAPIError_ может быть присвоено значение NULL, если поставщик не может предоставить структуру **MAPIERROR** , используя соответствующие сведения. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и поставщик адресной книги не поддерживает Юникод, или MAPI_UNICODE не было установлено и поддерживает только Юникод в адресной книге.
    
## <a name="remarks"></a>Замечания

Метод **GetLastError** для предоставления сведений о предыдущий вызов, завершившихся сбоем, реализуемые поставщиками адресных книг. Вызывающие объекты можно предоставить своим пользователям подробные сведения об ошибке, включая данные из структуры **MAPIERROR** в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать структуры **MAPIERROR** , на который указывает параметр _lppMAPIError_ , если поставщик адресной книги предоставляет структуру и **код последней ошибки** возвращается значение S_OK. В некоторых случаях поставщик адресной книги не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит. В этом случае поставщик адресной книги возвращает указатель на значение NULL в _lppMAPIError_ вместо этого. 
  
Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

