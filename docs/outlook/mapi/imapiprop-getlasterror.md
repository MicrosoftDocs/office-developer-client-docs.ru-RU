---
title: имапипропжетластеррор
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435833"
---
# <a name="imapipropgetlasterror"></a>IMAPIProp::GetLastError

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущем сообщении об ошибке. 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a>Параметры

 _Состав_
  
> возврата Дескриптор кода ошибки, созданного при предыдущем вызове метода.
    
 _ulFlags_
  
> возврата Битовая маска флагов, указывающая формат текста, возвращаемого в структуре **мапиеррор** , на которую указывает _лппмапиеррор_. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строки должны быть в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки должны быть в формате ANSI.
    
 _лппмапиеррор_
  
> вышли Указатель на указатель на структуру **мапиеррор** , содержащую сведения о версии, компоненте и контексте ошибки. Параметр _лппмапиеррор_ может иметь значение null, если сведения об ошибке не возвращаются. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Возвращены сведения об ошибке.
    
MAPI_E_BAD_CHARWIDTH 
  
> Установлен флаг MAPI_UNICODE, а реализация не поддерживает Юникод, или MAPI_UNICODE не задано, а реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp:: GetLastError** предоставляет сведения о предыдущем вызове метода, который завершился сбоем. Клиенты могут предоставить пользователям подробные сведения об ошибке, включив данные из структуры **мапиеррор** в диалоговом окне. 
  
Все реализации **GetLastError** , ПРЕДОСТАВЛЯЕМые MAPI, являются реализациями ANSI, за исключением реализации [IAddrBook](iaddrbookimapiprop.md) . Метод **GetLastError** , включенный в **IAddrBook** , поддерживает Юникод. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Сведения о реализации этого метода для удаленного поставщика транспорта, а также о том, какие сообщения этот метод возвращает поставщику транспорта, так как определенные условия ошибок, ведущие к различным значениям HRESULT, будут отличаться для разных поставщиков транспорта.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно использовать структуру **мапиеррор** , на которую указывает параметр _Лппмапиеррор_ , если **GetLastError** содержит один, только если возвращаемое значение S_OK. Иногда **GetLastError** не может определить, что последняя ошибка или больше не содержит ничего больше, чтобы сообщить об ошибке. В этом случае указатель на NULL возвращается в _лппмапиеррор_ . 
  
Чтобы освободить память для структуры **мапиеррор** , вызовите функцию [мапифрибуффер](mapifreebuffer.md) . 
  
Дополнительные сведения о методе **GetLastError** приведены в разделе [Расширенные ошибки MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Расширенные ошибки MAPI](mapi-extended-errors.md)

