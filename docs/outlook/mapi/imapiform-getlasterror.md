---
title: IMAPIFormGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetLastError
api_type:
- COM
ms.assetid: 81af8a0b-4ec2-459c-8ab2-29d28a8b680f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8b29298ab97518c2e346c2cdc5dee6baec28f8e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808880"
---
# <a name="imapiformgetlasterror"></a>IMAPIForm::GetLastError

  
  
**Относится к**: Outlook 
  
Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибок, вызываемых объектом формы. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _hResult_
  
> [in] Тип данных HRESULT, которое содержит значение ошибки, созданный в предыдущем вызове метода.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее тип возвращаемой строки. Можно задать следующий флаг: 
    
MAPI_UNICODE 
  
> Если набор строк в структуре **MAPIERROR** , возвращаемые в параметре _lppMAPIError_ , в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на структуру возвращенные **MAPIERROR** , версии, компонент и контекста сведения об ошибке. Этот параметр может быть присвоено значение NULL, если структура не **MAPIERROR** для возврата. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и **GetLastError** не поддерживает Юникод, или MAPI_UNICODE не было установлено и **GetLastError** поддерживает только Юникод. 
    
## <a name="remarks"></a>Замечания

Метод **IMAPIForm::GetLastError** предоставляет сведения о предыдущий вызов, завершившихся сбоем. Вызывающие объекты можно предоставить своим пользователям подробные сведения об ошибке, включая данные из структуры **MAPIERROR** в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать структуры **MAPIERROR** , на который указывает параметр _lppMAPIError_ Если MAPI предоставляет, только в том случае, если **код последней ошибки** возвращается значение S_OK. В некоторых случаях MAPI не может определить последнюю ошибку был или он не более сообщить об ошибке содержит. В этом случае указатель на значение NULL, возвращается в _lppMAPIError_ вместо этого. 
  
Дополнительные сведения о методе **GetLastError** отображаются [С помощью расширенных ошибки](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

