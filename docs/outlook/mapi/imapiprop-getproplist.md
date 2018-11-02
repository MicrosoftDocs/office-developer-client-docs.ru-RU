---
title: IMAPIPropGetPropList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5417853dbb1fa87d2beead2f73ca57329e17b044
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571124"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает свойство теги для всех свойств. 
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который управляет формата для строк в тегах возвращаемого свойства. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> В формате Юникод, возвращенных строк. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
 _lppPropTagArray_
  
> [out] Указатель на указатель массив тег свойство, которое содержит теги для всех свойств объекта.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Все теги свойство были успешно возвращен.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp::GetPropList** получает тега свойства для каждого свойства, в настоящее время поддерживается объектом. Если объект не поддерживает все свойства, **GetPropList** возвращает массив свойство тег с элементом **cValues** значение 0. 
  
Область свойств, возвращаемых **GetPropList** зависит от поставщика для поставщика. Некоторые поставщики услуг исключать эти свойства, для которых вызывающий не имеет доступа. Все поставщики возврата свойств типа **PT_OBJECT**.
  
Если объект не поддерживает Юникод, **GetPropList** возвращает MAPI_E_BAD_CHARWIDTH, даже в том случае, если нет строки свойств, определенных для объекта. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Поставщики удаленного транспорта реализовать **GetPropList** именно то, как указано здесь. Существуют нет специальных проблемы. Реализация Конечно, вернет тот же список свойства, как поддерживаемый метод [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) , чтобы освободить место на массива тега свойства, на который указывает _lppPropTagArray_. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |Mfcmapi (en) использует метод **IMAPIProp::GetPropList** , чтобы получить список свойств для передачи **GetProps**.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

