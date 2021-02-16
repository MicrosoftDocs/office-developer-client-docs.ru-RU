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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Обновляет одно или несколько свойств.
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Параметры

 _cValues_
  
> [in] Количество значений свойств, на которые указывает параметр _lpPropArray._ Параметр  _cValues не_ должен быть 0. 
    
 _lpPropArray_
  
> [in] Указатель на массив структур [SPropValue,](spropvalue.md) содержащих значения свойств для обновления. 
    
 _lppProblems_
  
> [in, out] При вводе указатель на указатель на [структуру SPropProblemArray;](spropproblemarray.md) в противном случае NULL, указывающее на отсутствие необходимости в сведениях об ошибках. Если  _lppProblems_ является допустимым указателем при вводе, **SetProps** возвращает подробные сведения об ошибках при обновлении одного или более свойств. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Свойства были успешно обновлены.
    
Следующие значения могут быть возвращены в структуре **SPropProblemArray,** но не в качестве возвращаемой величины **для SetProps:**
  
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
MAPI_E_COMPUTED 
  
> Свойство не может быть обновлено, так как оно является "только чтением", вычисляется поставщиком услуг, отвечающим за объект.
    
MAPI_E_INVALID_TYPE 
  
> Недопустимый тип свойства.
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка изменить объект, доступный только для чтения, или получить доступ к объекту, у которого у пользователя недостаточно разрешений.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Свойство не может быть обновлено, так как оно больше размера буфера удаленного вызова процедур (RPC).
    
MAPI_E_UNEXPECTED_TYPE 
  
> Тип свойства не является типом, ожидаемым реализацией вызова.
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Игнорируйте **тег PR_NULL** ([PidTagNull)](pidtagnull-canonical-property.md)и все свойства с типом PT_ERROR **.** Не внося изменений и не сообщая о проблемах в **структуре SPropProblemArray.** 
  
Возвращает MAPI_E_INVALID_PARAMETER, если свойство типа **PT_OBJECT** включено в массив значений свойств. Также возвращает эту ошибку, если свойство с несколькими значениями включено в массив и его член **cValues** имеет значение 0. 
  
Если вызов в целом был успешным, но при этом возникли проблемы с настройкой некоторых свойств, верните S_OK и поместите сведения о проблемах в соответствующую запись структуры **SPropProblemArray,** на которую указывает параметр _lppProblems._ 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

В зависимости от поставщика службы можно также изменить тип свойства, передав тег свойства, содержащий тип, отличающийся от ранее использованного с заданным идентификатором свойства.
  
Если вы включаете тег свойства, неподключенный объектом, и реализация **SetProps** позволяет создавать новые свойства, свойство добавляется в объект. Любое предыдущее значение, сохраненное с идентификатором свойства, которое использовалось для нового свойства, удаляется. 
  
Обратите внимание S_OK возвращаемого значения не гарантирует, что все свойства были успешно обновлены. Некоторые поставщики кэшют вызовы **SetProps,** пока не получат вызов, требуя вмешательства поставщика, например [IMAPIProp::SaveChanges](imapiprop-savechanges.md) или [IMAPIProp::GetProps.](imapiprop-getprops.md) Таким образом, можно получить значения ошибок, которые относятся к **вызову SetProps** с последующими вызовами. 
  
Если **SetProps** возвращает S_OK, проверьте структуру **SPropProblemArray,** на которая указывает  _lppProblems,_ на проблемы при обновлении отдельных свойств. Если **SetProps** возвращает ошибку, не проверяйте массив проблем свойств. Вместо этого вызовите метод [IMAPIProp::GetLastError](imapiprop-getlasterror.md) объекта. 
  
При обновлении больших свойств **SetProps** может привести к сбойу и возврату MAPI_E_NOT_ENOUGH_MEMORY. Для свойств не существует максимального размера, и разные объекты могут иметь разные ограничения. Если вы имеете дело с потенциально большими свойствами, будьте готовы вызвать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с IID_IStream в качестве идентификатора интерфейса, если **SetProps** возвращает это значение ошибки. 
  
Вызовите [функцию MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить **структуру SPropProblemArray.** 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|PropertyEditor.cpp  <br/> |CPropertyEditor::WriteSPropValueToObject  <br/> |MFCMAPI использует метод **IMAPIProp::SetProps** для записи свойства обратно в объект после изменения свойства.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)

