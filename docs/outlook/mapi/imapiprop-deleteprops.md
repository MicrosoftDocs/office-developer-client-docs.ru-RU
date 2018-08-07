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
ms.openlocfilehash: 8eb19f9a2d3458e153b0758b56c502ce612be0cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809044"
---
# <a name="imapipropdeleteprops"></a>IMAPIProp::DeleteProps

  
  
**Относится к**: Outlook 
  
Удаляет одно или несколько свойств объекта. 
  
```cpp
HRESULT DeleteProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Параметры

 _lpPropTagArray_
  
> [in] Указатель на массив тегов свойств, которые указывают свойства, которые нужно удалить. Член **cValues** структуры [SPropTagArray](sproptagarray.md) , на который указывает _lpPropTagArray_ не должна быть нулевой и сам параметр _lpPropTagArray_ не должна быть NULL. 
    
 _lppProblems_
  
> [in, out] На входе указатель указатель на структуру [SPropProblemArray](spropproblemarray.md) ; в противном случае — значение NULL, который означает, что нет необходимости для получения сведений об ошибках. Если _lppProblems_ допустимый указатель на входные данные, **DeleteProps** возвращает подробные сведения об ошибках в удаления одного или нескольких свойств. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Свойства были успешно удалены.
    
MAPI_E_NO_ACCESS 
  
> Вызывающий не имеет разрешений на удаление свойства.
    
## <a name="remarks"></a>Замечания

Метод **IMAPIProp::DeleteProps** удаляет одного или нескольких свойств из текущего объекта. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Необходимо разрешить свойства к удалению из всех объектов. Если объект не является изменяемым, возвратите MAPI_E_NO_ACCESS из метода **DeleteProps** . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Задать тип свойства для каждого свойства тега в массиве тег свойство указывает параметр _lpPropTagArray_ не нужно. Типы свойств игнорируются; используются только идентификаторы свойств. 
  
Обратите внимание, что некоторые объекты не разрешать изменений и возврата, что эти объекты MAPI_E_NO_ACCESS из метода **DeleteProps** . Другие объекты разрешить некоторые свойства к удалению, но не для других пользователей. При наличии проблем удаление только некоторые свойства, **DeleteProps** возвращает значение S_OK. Если допустимый указатель выполнены в параметре _lppProblems_ , **DeleteProps** установит указатель на структуру **SPropProblemArray** , который содержит подробные сведения о проблемах, связанных с каждого свойства. Например при удалении все свойства сообщения и проблемы с одним или несколькими его вложения, структура **SPropProblemArray** будет содержать запись для **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments ](pidtagmessageattachments-canonical-property.md)) свойство. 
  
Структура, на который указывает _lppProblems_ допустимо только в том случае, если **DeleteProps** возвращает значение S_OK. Если **DeleteProps** возвращает ошибку, не следует использовать структуру **SPropProblemArray** . Вместо этого вызов метода [IMAPIProp::GetLastError](imapiprop-getlasterror.md) объекта для получения дополнительных сведений об ошибке. 
  
Бесплатная загрузка возвращенные структура **SPropProblemArray** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |DeleteProperty  <br/> |Mfcmapi (en) использует метод **IMAPIProp::DeleteProps** , чтобы удалить свойство из объекта.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

