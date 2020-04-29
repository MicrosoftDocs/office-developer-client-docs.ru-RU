---
title: иперсистмессажежетластеррор
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetLastError
api_type:
- COM
ms.assetid: 32cc3a1f-1310-4788-b0f4-93c1e4940f37
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2189a39e115236e6c2ec9de8a263ce3982d8b8e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426711"
---
# <a name="ipersistmessagegetlasterror"></a>IPersistMessage::GetLastError

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущем сообщении об ошибке в объекте Form. 
  
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
  
> вышли Указатель на указатель на структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки. Параметр _лппмапиеррор_ может иметь значение null, если форма не может предоставить соответствующую информацию для структуры **мапиеррор** . 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Установлен флаг MAPI_UNICODE, а поставщик адресных книг не поддерживает Юникод или MAPI_UNICODE не задан, а поставщик адресных книг поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Объекты Form реализуют метод **иперсистмессаже:: GetLastError** для предоставления сведений о предыдущем вызове метода, который завершился неудачно. Средства просмотра форм могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры [мапиеррор](mapierror.md) в диалоговом окне. 
  
Вызов **GetLastError** не влияет на состояние формы. Когда функция **GetLastError** возвращает результат, форма остается в состоянии, в котором она находилась до совершения вызова. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Структуру **мапиеррор** можно использовать, если в форме есть одна, на которую указывает параметр _лппмапиеррор_ , только если **GetLastError** возвращает S_OK. Иногда форма не может определить, в чем последняя ошибка, или больше не может сообщить об ошибке. В этом случае форма возвращает указатель на значение NULL в _лппмапиеррор_ вместо этого. 
  
Дополнительные сведения о методе **GetLastError** приведены в разделе [Расширенные ошибки MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

