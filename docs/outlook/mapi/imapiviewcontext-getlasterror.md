---
title: имапивиевконтекстжетластеррор
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetLastError
api_type:
- COM
ms.assetid: 3306e37a-2500-4281-96c3-ca0d5c81909d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bcd8e977d924bae170dcad27c672b963189cfa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424429"
---
# <a name="imapiviewcontextgetlasterror"></a>IMAPIViewContext::GetLastError

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, возникшей в объекте контекста представления. 
  
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
  
> Строки в структуре **мапиеррор** , возвращаемые в параметре _лппмапиеррор_ , представлены в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI. 
    
 _лппмапиеррор_
  
> вышли Указатель на указатель на возвращаемую структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки. Этот параметр может иметь значение NULL, если структура **мапиеррор** для возврата отсутствует. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Установлен флаг MAPI_UNICODE, а **GetLastError** не поддерживает Юникод, или MAPI_UNICODE не задано, а **GetLastError** поддерживает только Юникод. 
    
## <a name="remarks"></a>Примечания

Метод **имапивиевконтекст:: GetLastError** предоставляет сведения о предыдущем вызове метода, который завершился сбоем. Вызывающие абоненты могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **мапиеррор** в диалоговом окне. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать структуру **мапиеррор** , на которую указывает параметр _ЛППМАПИЕРРОР_ , если MAPI поддерживает один, только если **GetLastError** возвращает S_OK. Иногда MAPI не может определить, какая ошибка прошла или больше не может сообщить об ошибке. В этом случае указатель на NULL возвращается в _лппмапиеррор_ . 
  
Дополнительные сведения о методе **GetLastError** приведены в разделе [Расширенные ошибки MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

