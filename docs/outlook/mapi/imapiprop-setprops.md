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
ms.openlocfilehash: 87709f8a77471637d7652982669bcba93ca2e1dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412620"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Обновляет одно или несколько свойств.
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parameters

 _cValues_
  
> [in] Количество значений свойств, на которые указывает _параметр lpPropArray._ Параметр  _cValues_ не должен быть 0. 
    
 _lpPropArray_
  
> [in] Указатель на массив [структур SPropValue,](spropvalue.md) содержащих обновляемые значения свойств. 
    
 _lppProblems_
  
> [in, out] На входе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае NULL, указывающая на отсутствие необходимости в сведениях об ошибках. Если  _lppProblems_ является допустимым указателем ввода, **SetProps** возвращает подробные сведения об ошибках при обновлении одного или более свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства были успешно обновлены.
    
Следующие значения могут быть возвращены в **структуре SPropProblemArray,** но не в качестве значений возврата **для SetProps:**
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
MAPI_E_COMPUTED 
  
> Свойство не может быть обновлено, так как оно только для чтения, вычисляется поставщиком услуг, отвечающим за объект.
    
MAPI_E_INVALID_TYPE 
  
> Тип свойства недействителен.
    
MAPI_E_NO_ACCESS 
  
> Была предпринята попытка изменить объект только для чтения или получить доступ к объекту, для которого у пользователя недостаточно разрешений.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Свойство не может быть обновлено, так как оно больше размера буфера удаленного вызова процедуры (RPC).
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не является типом, ожидаемым реализацией вызова.
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Игнорировать тег **свойства PR_NULL** [(PidTagNull)](pidtagnull-canonical-property.md)и все свойства с **типом PT_ERROR**. Не внося изменений или отчетов о проблемах в **структуре SPropProblemArray.** 
  
Возврат MAPI_E_INVALID_PARAMETER, если свойство **типа** PT_OBJECT включено в массив значений свойства. Также возвращаем эту ошибку, если свойство с несколькими значениями включено в массив и его **член cValues** задает значение 0. 
  
Если вызов удается в целом, но есть проблемы с установкой некоторых свойств, верните S_OK и поместите сведения о проблемах в соответствующую запись **структуры SPropProblemArray,** на которую указывает параметр _lppProblems._ 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

В зависимости от поставщика услуг вы также можете изменить тип свойства, передав тег свойства, содержащий другой тип, чем был ранее использован с заданным идентификатором свойства.
  
Если вы включаете тег свойства для свойства, которое неподтверчено объекту, а реализация **SetProps** позволяет создавать новые свойства, свойство добавляется к объекту. Любое предыдущее значение, сохраненное с идентификатором свойства, которое использовалось для нового свойства, удаляется. 
  
Обратите внимание, S_OK значение возврата не гарантирует успешное обновление всех свойств. Некоторые поставщики кэша **Вызовы SetProps,** пока они не получат вызов, который требует вмешательства поставщика, такие как [IMAPIProp::SaveChanges](imapiprop-savechanges.md) или [IMAPIProp::GetProps](imapiprop-getprops.md). Таким образом, можно получать значения ошибок, которые относятся к **вызову SetProps** с последующими вызовами. 
  
Если **SetProps** возвращается S_OK, проверьте структуру **SPropProblemArray,** на которые указывает  _lppProblems,_ на проблемы с обновлением отдельных свойств. Если **SetProps** возвращает ошибку, не проверяйте массив проблем свойств. Вместо этого позвоните по методу [IMAPIProp::GetLastError.](imapiprop-getlasterror.md) 
  
При обновлении больших свойств **SetProps** может привести к сбойу и возвращению MAPI_E_NOT_ENOUGH_MEMORY. Для свойств не существует максимального размера, а у разных объектов могут быть разные ограничения. Если вы имеете дело с потенциально большими свойствами, будьте готовы вызвать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с IID_IStream в качестве идентификатора интерфейса, если **SetProps** возвращает это значение ошибки. 
  
Вызов [функции MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить **структуру SPropProblemArray.** 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|PropertyEditor.cpp  <br/> |CPropertyEditor::WriteSPropValueToObject  <br/> |MFCMAPI использует метод **IMAPIProp::SetProps** для записи свойства обратно к объекту после редактирования свойства.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)

