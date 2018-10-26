---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 93bfcce9c45a4c6fd4d57be8c1222be286e0a945
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592033"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Обновление одного или нескольких свойств.
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Параметры

 _cValues_
  
> [in] Количество значений свойств, на который указывает параметр _lpPropArray_ . Параметр _cValues_ не должен иметь значение 0. 
    
 _lpPropArray_
  
> [in] Указатель на массив структур [SPropValue](spropvalue.md) , которые содержат значения свойств, который требуется обновить. 
    
 _lppProblems_
  
> [in, out] На входе указатель указатель на структуру [SPropProblemArray](spropproblemarray.md) ; в противном случае — значение NULL, указывающее, не требуется выполнять сведения об ошибке. Если _lppProblems_ допустимый указатель на входные данные, **SetProps** возвращает подробные сведения об ошибках при обновлении одного или нескольких свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства были успешно обновлены.
    
Возможные значения могут быть возвращены в структуре **SPropProblemArray** , но не как возвращаемые значения для **SetProps**:
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
MAPI_E_COMPUTED 
  
> Свойство не может быть обновлен, поскольку он доступен только для чтения, вычисленный с поставщиком, который несет ответственность за объект.
    
MAPI_E_INVALID_TYPE 
  
> Недопустимый тип свойства.
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка изменения объекта только для чтения или для доступа к объекту, для которого пользователь имеет недостаточно разрешений.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Не удается обновить свойство, так как они больше, чем размер буфера удаленного вызова (RPC).
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не типа, вызывающий реализации.
    
## <a name="notes-to-implementers"></a>Примечания для реализующих

Игнорируйте все свойства с типом **PT_ERROR**и тег свойства **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)). Не вносить изменения или отправки отчетов о проблемах в структуре **SPropProblemArray** . 
  
Возвращает MAPI_E_INVALID_PARAMETER, если свойство типа **PT_OBJECT** включен в массиве значение свойства. Также возвращает эту ошибку, если свойство несколько значений входит в массиве и его элементом **cValues** имеет значение 0. 
  
Если звонок успешно в целом, но существуют проблемы с указанием некоторые свойства, возвращает значение S_OK и поместить сведения о проблемах в соответствии структуры **SPropProblemArray** , параметр _lppProblems_ . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

В зависимости от поставщика услуг может быть возможность изменить тип свойства, передав свойство тега, содержащего другого типа, не использовался ранее с идентификатором данного свойства.
  
Если включить тег свойства для свойства, которое не поддерживается объектом и реализации **SetProps** позволяет создавать новые свойства, свойство добавлен в объект. Предыдущее значение хранятся с идентификатором свойства, который использовался для нового свойства удаляются. 
  
Обратите внимание на то, что значение, возвращаемое значение S_OK не гарантирует, что все свойства были успешно обновлены. Некоторые поставщики кэширование **SetProps** вызовы, пока они получают звонок, который требует вмешательства поставщика, например [IMAPIProp::SaveChanges](imapiprop-savechanges.md) или [IMAPIProp::GetProps](imapiprop-getprops.md). Таким образом можно получать значения ошибок, имеющих отношение к звонку **SetProps** со звонками более поздней версии. 
  
Если **SetProps** возвращает значение S_OK, проверьте **SPropProblemArray** структуры, на который указывает _lppProblems_ для проблем в процессе обновления отдельных свойств. Если **SetProps** возвращает ошибку, не устанавливайте массива свойства проблемы. Вместо этого вызов метода [IMAPIProp::GetLastError](imapiprop-getlasterror.md) объекта. 
  
При обновлении большого свойств, **SetProps** может давать сбой и возвращать MAPI_E_NOT_ENOUGH_MEMORY. Максимальный размер для свойства не и разных объектов могут иметь разные ограничения. При работе с потенциально большого свойства быть подготовлен для вызова метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с IID_IStream идентификатор интерфейса, если **SetProps** возвращает значение этой ошибки. 
  
Вызовите функцию [MAPIFreeBuffer](mapifreebuffer.md) , чтобы освободить место на **SPropProblemArray** структуры. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|PropertyEditor.cpp  <br/> |CPropertyEditor::WriteSPropValueToObject  <br/> |Mfcmapi (en) использует метод **IMAPIProp::SetProps** для обратной записи свойства объекта после изменения свойства.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)

