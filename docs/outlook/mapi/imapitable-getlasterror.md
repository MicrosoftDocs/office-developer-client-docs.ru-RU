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
ms.openlocfilehash: 2444ea7e05367423e7920be3a871c2ab68aad76d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419004"
---
# <a name="imapitablegetlasterror"></a>IMAPITable::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает [структуру MAPIERROR, содержащую](mapierror.md) сведения о предыдущей ошибке в таблице. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Parameters

 _hResult_
  
> [in] HRESULT, содержащая ошибку, созданную в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Bitmask флагов, которые контролируют тип возвращаемой строки. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI. 
    
 _lppMAPIError_
  
> [вышел] Указатель на указатель на возвращаемую структуру **MAPIERROR,** содержащую сведения о версии, компоненте и контексте для ошибки. Параметр  _lppMAPIError может_ быть задан в NULL, если структура **MAPIERROR** с соответствующей информацией не может быть предоставлена. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::GetLastError** возвращает подробные сведения, если они доступны, о сбойного вызова предыдущего метода. Эти сведения можно отображать в сообщении или диалоговом окне. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

**Вызывай GetLastError всякий** раз, когда необходимо отобразить сведения об ошибке пользователю. 
  
Вы можете использовать структуру [MAPIERROR,](mapierror.md) на что указывает параметр  _lppMAPIError,_ если объект таблицы поставляет один только в том случае, если **GetLastError** возвращает S_OK. Иногда реализация таблицы не может определить, какая была последняя ошибка, или больше не имеет ничего, чтобы сообщить об ошибке. В этой ситуации указатель  _на lppMAPIError_ заданной nULL. 
  
Чтобы освободить всю память, выделенную для **структуры MAPIERROR,** позвоните [в функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
Дополнительные сведения о **методе GetLastError** см. в дополнительных сведениях [о расширенных ошибках MAPI.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

