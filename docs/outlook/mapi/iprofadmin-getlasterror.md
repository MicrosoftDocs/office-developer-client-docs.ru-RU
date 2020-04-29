---
title: ипрофадминжетластеррор
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
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b6964ecde3a78bd1e9ce0ae1dcab0342c5a21a03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430775"
---
# <a name="iprofadmingetlasterror"></a>IProfAdmin::GetLastError

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, возникшей в объекте администрирования профиля. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _Состав_
  
> возврата Тип данных HRESULT, который содержит значение ошибки, возникшей при предыдущем вызове метода.
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющих тип возвращаемых строк. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре [мапиеррор](mapierror.md) , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI. 
    
 _лппмапиеррор_
  
> вышли Указатель на указатель на структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки. Параметр _лппмапиеррор_ может иметь значение null, если структура **мапиеррор** для возврата отсутствует. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Установлен флаг MAPI_UNICODE, а реализация не поддерживает Юникод, или MAPI_UNICODE не задано, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Метод **ипрофадмин:: GetLastError** получает сведения о последней ошибке, возвращенной при вызове метода для объекта администрирования профиля. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Структуру **мапиеррор** можно использовать, если она предоставляет MAPI, на которую указывает параметр _лппмапиеррор_ , только если **GetLastError** возвращает S_OK. Иногда MAPI не может определить, какая ошибка прошла или больше не может сообщить об ошибке. В этом случае указатель на NULL возвращается в _лппмапиеррор_. 
  
Чтобы освободить всю память, выделенную MAPI для структуры **мапиеррор** , вызовите функцию [мапифрибуффер](mapifreebuffer.md) . 
  
Более подробную информацию о методе **GetLastError** можно узнать [в статье Использование расширенных ошибок](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

