---
title: IMsgServiceAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetLastError
api_type:
- COM
ms.assetid: 9e3c8d6e-74be-46a7-94ed-74a969caf165
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 7ce81e419a4092bd99e5082810ea9d08cb2cc163
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809365"
---
# <a name="imsgserviceadmingetlasterror"></a>IMsgServiceAdmin::GetLastError

  
  
**Применимо к**: Outlook 
  
Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о последней ошибке, возникшей для объекта message службы администрирования. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] Тип данных HRESULT, которое содержит значение ошибки, созданный предыдущей вызова метода.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип возвращаемой строки. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на структуру возвращенные **MAPIERROR** , версии, компонент и контекста сведения об ошибке. Параметр _lppMAPIError_ может быть присвоено значение NULL, если структура не **MAPIERROR** для возврата. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Был установлен флажок MAPI_UNICODE и объект администрирования службы сообщений не поддерживает Юникод.
    
## <a name="remarks"></a>Замечания

Метод **IMsgServiceAdmin::GetLastError** получает сведения о последней ошибки, возвращаемые для вызова метода [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Клиенты можно предоставить своим пользователям подробные сведения об ошибке, включая эти сведения в диалоговом окне. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы использовать **MAPIERROR** структуры, если MAPI предоставляет, на который указывает параметр _lppMAPIError_ только в том случае, если **код последней ошибки** возвращается значение S_OK. В некоторых случаях MAPI не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит. В этом случае **GetLastError** возвращает указатель на значение NULL в _lppMAPIError_ вместо этого. 
  
Дополнительные сведения о методе **GetLastError** отображаются [С помощью расширенных ошибки](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgServiceAdmin: IUnknown](imsgserviceadminiunknown.md)

