---
title: IProfAdminGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetLastError
api_type:
- COM
ms.assetid: bb161d7b-ae5b-4f8e-a506-8346ac5e583d
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 250074b28b98269df58fecfcb2d178f73e26c571
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809503"
---
# <a name="iprofadmingetlasterror"></a>IProfAdmin::GetLastError

  
  
**Применимо к**: Outlook 
  
Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибки, которые произошли в объект администрирования профилей. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] Тип данных HRESULT, которое содержит значение ошибки, созданный в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип возвращаемой строки. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре [MAPIERROR](mapierror.md) , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки. Параметр _lppMAPIError_ может быть присвоено значение NULL, если структура не **MAPIERROR** для возврата. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Замечания

Метод **IProfAdmin::GetLastError** получает сведения о последней ошибки, возвращаемые при вызове метода для объекта администрирования профилей. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Структура **MAPIERROR** , можно использовать, если MAPI предоставляет, на который указывает только если параметр _lppMAPIError_ **GetLastError** возвращает значение S_OK. В некоторых случаях MAPI не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит. В этом случае указатель на значение NULL, возвращается в _lppMAPIError_. 
  
Для освобождения всех памяти, выделенной для структуры **MAPIERROR** MAPI, вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Дополнительные сведения о методе **GetLastError** отображаются [С помощью расширенных ошибки](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IProfAdmin: IUnknown](iprofadminiunknown.md)

