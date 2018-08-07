---
title: IPersistMessageGetLastError
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
ms.openlocfilehash: 16f091f4d9527cd82ebc1d1eadee2fb55b481929
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809492"
---
# <a name="ipersistmessagegetlasterror"></a>IPersistMessage::GetLastError

  
  
**Относится к**: Outlook 
  
Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущей ошибки в объекте формы. 
  
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
  
> Строки в структуре [MAPIERROR](mapierror.md) , возвращаемые в параметре _lppMAPIError_ хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI. 
    
 _lppMAPIError_
  
> [out] Указатель на указатель на структуру **MAPIERROR** , который содержит сведения о версии, компонент и контекста для ошибки. Параметр _lppMAPIError_ может быть присвоено значение NULL, если форма не может предоставить соответствующие сведения для структуры **MAPIERROR** . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и поставщик адресной книги не поддерживает Юникод, или MAPI_UNICODE не было установлено и поддерживает только Юникод в адресной книге.
    
## <a name="remarks"></a>Замечания

Объекты формы реализуйте метод **IPersistMessage::GetLastError** для предоставления сведений о предыдущий вызов, завершившихся сбоем. Средства просмотра формы может предоставить их пользователям с подробными сведениями об ошибке, включая данные из структуры [MAPIERROR](mapierror.md) в диалоговое окно. 
  
Вызов **GetLastError** не влияет на состояние формы. Когда **код последней ошибки** возвращается, форма остается в состоянии, он находился до звонка. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Структура **MAPIERROR** , можно использовать, если форма предоставляет, который указывает с помощью параметра _lppMAPIError_ только в том случае, если **код последней ошибки** возвращается значение S_OK. В некоторых случаях форма не может определить, что последнее сообщение об ошибке была или Дополнительно, чтобы сообщить об ошибке не содержит. В этой ситуации форма возвращает указатель на значение NULL в _lppMAPIError_ вместо этого. 
  
Дополнительные сведения о методе **GetLastError** отображаются [Ошибки расширенного MAPI](mapi-extended-errors.md).
  
## <a name="see-also"></a>См. также



[MAPIERROR](mapierror.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)

