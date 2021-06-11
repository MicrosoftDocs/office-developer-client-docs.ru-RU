---
title: IMAPIPropDeleteProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.DeleteProps
api_type:
- COM
ms.assetid: 5cc642de-21f0-4826-bf21-aac4bcfc1328
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5bfef87baa2dffa4605f9a7afa3833024f514430
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409239"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет одно или несколько свойств из объекта. 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameters

 _lpPropTagArray_
  
> [in] Указатель на массив тегов свойств, которые указывают свойства, которые необходимо удалить. Член **cValues** структуры [SPropTagArray,](sproptagarray.md) на который указывает  _lpPropTagArray,_ не должен быть нулем, а сам  _параметр lpPropTagArray_ не должен быть NULL. 
    
 _lppProblems_
  
> [in, out] На входе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае NULL, что указывает на отсутствие необходимости в сведениях об ошибках. Если  _lppProblems_ является допустимым указателем на ввод, **DeleteProps** возвращает подробные сведения об ошибках при удалении одного или более свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства были успешно удалены.
    
MAPI_E_NO_ACCESS 
  
> У вызываемого недостаточно разрешений на удаление свойств.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp::D eleteProps** удаляет одно или несколько свойств из текущего объекта. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Не нужно разрешать удалять свойства из всех объектов. Если объект не может быть модификабельным, MAPI_E_NO_ACCESS из **метода DeleteProps.** 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Не нужно устанавливать тип свойства для каждого тега свойств в массиве тегов свойств, на которые указывает параметр _lpPropTagArray._ Типы свойств игнорируются; используются только идентификаторы свойств. 
  
Следует помнить, что некоторые объекты не позволяют вносить изменения и что MAPI_E_NO_ACCESS возвращаются из **метода DeleteProps.** Другие объекты позволяют удалять некоторые свойства, но не другие. При проблеме удаления только некоторых свойств **DeleteProps** возвращает S_OK. Если вы передали допустимый указатель в  _параметре lppProblems,_ **DeleteProps** задает указатель структуре **SPropProblemArray,** которая содержит подробные сведения о проблемах с каждым свойством. Например, если удалить все свойства сообщения и возникла проблема с одним или несколькою его вложениями, структура **SPropProblemArray** будет содержать запись для **свойства PR_MESSAGE_ATTACHMENTS** [(PidTagMessageAttachments).](pidtagmessageattachments-canonical-property.md) 
  
Структура, на которые указывает  _lppProblems,_ действительна только в том случае, если **DeleteProps** возвращает S_OK. Если **DeleteProps** возвращает ошибку, не пытайтесь использовать **структуру SPropProblemArray.** Вместо этого позвоните по методу [IMAPIProp::GetLastError,](imapiprop-getlasterror.md) чтобы получить дополнительные сведения об ошибке. 
  
Освободите возвращенную **структуру SPropProblemArray,** назвав [функцию MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |MFCMAPI использует метод **IMAPIProp::D eleteProps** для удаления свойства объекта.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

