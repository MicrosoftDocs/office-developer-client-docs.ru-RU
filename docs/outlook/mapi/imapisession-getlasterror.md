---
title: Имаписессионжетластеррор
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
ms.openlocfilehash: 7477213ee854be1ae71b47a0c1b339c4c13b6f04
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435581"
---
# <a name="imapisessiongetlasterror"></a>IMAPISession::GetLastError

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [мапиеррор](mapierror.md) , содержащую сведения об ошибке предыдущего сеанса. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _Состав_
  
> возврата Дескриптор значения ошибки, возникшей при предыдущем вызове метода.
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющих тип возвращаемых строк. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **мапиеррор** , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI. 
    
 _Лппмапиеррор_
  
> вышли Указатель на указатель на структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки. Параметр _лппмапиеррор_ может иметь значение null, если MAPI не может предоставить соответствующую информацию для структуры **мапиеррор** . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
МАПИ_Е_БАД_ЧАРВИДС 
  
> Установлен флаг МАПИ_УНИКОДЕ, а сеанс не поддерживает Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession:: GetLastError** получает сведения о последней ошибке, возвращенной вызовом метода **IMAPISession** . Клиенты могут предоставить пользователям подробные сведения об ошибке, включив эти сведения в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Структуру **мапиеррор** можно использовать, если она предоставляет MAPI, на которую указывает параметр _лппмапиеррор_ , только если **GetLastError** возвращает значение S_OK. Иногда MAPI не может определить, какая Последняя ошибка, или больше не содержит ничего больше об ошибке. В этом случае **GetLastError** возвращает указатель на значение NULL в _лппмапиеррор_ . 
  
Дополнительные сведения о методе **GetLastError** приведены в разделе [Расширенные ошибки MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Расширенные ошибки MAPI](mapi-extended-errors.md)

