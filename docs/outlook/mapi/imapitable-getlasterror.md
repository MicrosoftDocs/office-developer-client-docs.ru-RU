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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [MAPIERROR, содержащую](mapierror.md) сведения о предыдущей ошибке в таблице. 
  
```cpp
HRESULT GetLastError(
HRESULT hResult,
ULONG ulFlags,
LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _hResult_
  
> [in] HRESULT, содержащий ошибку, созданную в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет типом возвращаемой строки. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **MAPIERROR,** возвращаемой в  _параметре lppMAPIError,_ имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на возвращенную структуру **MAPIERROR,** содержащую сведения о версии, компоненте и контексте для ошибки. Параметр  _lppMAPIError_ может иметь NULL, если не удается получить структуру **MAPIERROR** с соответствующими сведениями. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPITable::GetLastError** возвращает подробные сведения (если они доступны) о вызове предыдущего метода, который не удалось вызвать. Эти сведения могут отображаться в сообщении или диалоговом окне. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызовите **GetLastError** всякий раз, когда необходимо отобразить сведения об ошибке для пользователя. 
  
Вы можете использовать структуру [MAPIERROR,](mapierror.md) на которая указывает параметр  _lppMAPIError,_ если объект таблицы указывает ее только в том случае, если **GetLastError** возвращает S_OK. Иногда в реализации таблицы не удается определить, какая была последняя ошибка, или больше не нужно сообщать об ошибке. В этой ситуации для указателя  _на lppMAPIError_ устанавливается NULL. 
  
Чтобы освободить всю память, выделенную для структуры **MAPIERROR,** вызовите функцию [MAPIFreeBuffer.](mapifreebuffer.md) 
  
Дополнительные сведения о **методе GetLastError** см. в расширенных [ошибках MAPI.](mapi-extended-errors.md)
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)

