---
title: Имсгсервицеадминжетластеррор
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
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 302aebd0be78c833acf4f82d2bb815ba46ae6f77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317397"
---
# <a name="imsgserviceadmingetlasterror"></a>IMsgServiceAdmin::GetLastError

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о последней ошибке, произошедшей для объекта администрирования службы сообщений. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _Состав_
  
> возврата Тип данных HRESULT, который содержит значение ошибки, созданное предыдущим вызовом метода.
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющих тип возвращаемых строк. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки в структуре **мапиеррор** , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, строки представлены в формате ANSI. 
    
 _Лппмапиеррор_
  
> вышли Указатель на указатель на возвращаемую структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки. Параметр _лппмапиеррор_ может иметь значение null, если структура **мапиеррор** для возврата отсутствует. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
МАПИ_Е_БАД_ЧАРВИДС 
  
> Установлен флаг МАПИ_УНИКОДЕ, а объект администрирования службы сообщений не поддерживает Юникод.
    
## <a name="remarks"></a>Замечания

Метод **имсгсервицеадмин:: GetLastError** получает сведения о последней ошибке, возвращенной вызовом метода [имсгсервицеадмин](imsgserviceadminiunknown.md) . Клиенты могут предоставить пользователям подробные сведения об ошибке, включив эти сведения в диалоговое окно. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать структуру **мапиеррор** , если она предоставляет MAPI, на которую указывает параметр _лппмапиеррор_ , только если **GetLastError** возвращает значение S_OK. Иногда MAPI не может определить, какая ошибка прошла или больше не может сообщить об ошибке. В этом случае **GetLastError** возвращает указатель на значение NULL в _лппмапиеррор_ . 
  
Более подробную информацию о методе **GetLastError** можно узнать [в статье Использование расширенных ошибок](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)

