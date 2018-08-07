---
title: IMAPISessionGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetLastError
api_type:
- COM
ms.assetid: 38cb3692-a5f8-403a-9615-9bd5868af23c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 59b534a076aee6498be9146eabb69c62fca313ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809058"
---
# <a name="imapisessiongetlasterror"></a>IMAPISession::GetLastError

  
  
**Относится к**: Outlook 
  
Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущего сеанса. 
  
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
  
> [out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки. Параметр _lppMAPIError_ может быть присвоено значение NULL, если MAPI не может предоставить соответствующие сведения для структуры **MAPIERROR** . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Был установлен флажок MAPI_UNICODE и сеанса не поддерживает Юникод.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::GetLastError** получает сведения о последней ошибки, возвращаемые для вызова метода **IMAPISession** . Клиенты можно предоставить своим пользователям подробные сведения об ошибке, включая эти сведения в диалоговом окне. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Структура **MAPIERROR** , можно использовать, если MAPI предоставляет, на который указывает только если параметр _lppMAPIError_ **GetLastError** возвращает значение S_OK. В некоторых случаях MAPI не может определить последнюю ошибку был или он не более сообщить об ошибке содержит. В этом случае **GetLastError** возвращает указатель на значение NULL в _lppMAPIError_ вместо этого. 
  
Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Расширенных ошибки MAPI](mapi-extended-errors.md)

