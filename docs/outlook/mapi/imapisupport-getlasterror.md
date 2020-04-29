---
title: имаписуппортжетластеррор
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetLastError
api_type:
- COM
ms.assetid: 5b4290d9-230f-416a-9644-188578565c7b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c34c175c43ada03e982f08a27f675448ea24a567
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438549"
---
# <a name="imapisupportgetlasterror"></a>IMAPISupport::GetLastError

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения об ошибке предыдущего объекта поддержки. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _Состав_
  
> возврата Дескриптор значения ошибки, созданной в предыдущем вызове метода для объекта support.
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющих тип возвращаемых строк. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **мапиеррор** , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI. 
    
 _лппмапиеррор_
  
> вышли Указатель на указатель на структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки. Параметр _лппмапиеррор_ может иметь значение null, если не удается предоставить структуру **мапиеррор** с соответствующими сведениями об ошибках. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов выполнен успешно и вернул ожидаемое значение или значения.
    
MAPI_E_BAD_CHARWIDTH 
  
> Установлен флаг MAPI_UNICODE, а MAPI не поддерживает Юникод или MAPI_UNICODE не задан, а MAPI поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Метод **имаписуппорт:: GetLastError** реализован для всех объектов support. Вызывающие абоненты могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **мапиеррор** в диалоговом окне. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать указатель на структуру **мапиеррор** , если MAPI предоставляет один из параметров _лппмапиеррор_ , только если **GetLastError** возвращает S_OK. Иногда MAPI не может определить, в чем последняя ошибка, или сообщение об ошибке больше не содержит ничего. В этом случае _лппмапиеррор_ возвращает указатель на null вместо него. 
  
Дополнительные сведения о методе **GetLastError** приведены в разделе [Расширенные ошибки MAPI](mapi-extended-errors.md).
  
Чтобы освободить всю память, выделенную MAPI, вызовите функцию [мапифрибуффер](mapifreebuffer.md) для возвращенной структуры **мапиеррор** . 
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[Расширенные ошибки MAPI](mapi-extended-errors.md)

