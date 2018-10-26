---
title: IMAPITableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetLastError
api_type:
- COM
ms.assetid: 832e2c18-ddba-4d18-a391-710d21fe23e6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8b7b1db5bcc718858b01f122f53406c885998741
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593818"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR](mapierror.md) , содержащий сведения о предыдущем ошибки в таблице. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _hResult_
  
> [in] Значение HRESULT, содержащий ошибку, созданный в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип возвращенных строк. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на структуру возвращенные **MAPIERROR** , содержащий версии, компонент и контекста сведения об ошибке. Параметр _lppMAPIError_ может быть присвоено значение NULL, если структуру **MAPIERROR** , используя соответствующие сведения. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::GetLastError** возвращает подробные сведения, если он доступен, о вызов предыдущего метода, который не удалось. Эти сведения могут отображаться в сообщении или диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызов **GetLastError** каждый раз, когда необходимо отобразить сведения об ошибке для пользователя. 
  
Чтобы использовать [MAPIERROR](mapierror.md) структуры, на который указывает с помощью параметра _lppMAPIError_ Если объект таблицы его предоставляет только в том случае, если **код последней ошибки** возвращается значение S_OK. В некоторых случаях реализации таблицы не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит. В этом случае указатель мыши в _lppMAPIError_ имеет значение NULL. 
  
Для освобождения всех памяти, выделенный для структуры **MAPIERROR** , вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

