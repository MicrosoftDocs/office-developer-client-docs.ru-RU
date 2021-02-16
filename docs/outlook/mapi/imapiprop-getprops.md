---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9b03775d495f7d1f51142eb0ed06fc9ecdf6d1a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412459"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Извлекает значение свойства одного или более свойств объекта.
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a>Параметры

 _lpPropTagArray_
  
> [in] Указатель на массив тегов свойств, которые определяют свойства, значения которых необходимо получить. Параметр  _lpPropTagArray_ должен иметь значение NULL, указывающее на то, что должны быть возвращены значения для всех свойств объекта, или указать структуру [SPropTagArray,](sproptagarray.md) которая содержит один или несколько тегов свойств. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая указывает формат для свойств с типом PT_UNSPECIFIED. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Строки этих свойств должны возвращаться в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки должны возвращаться в формате ANSI.
    
 _lpcValues_
  
> [out] Указатель на количество значений свойств, на которые указывает параметр _lppPropArray._ Если  _lppPropArray_ имеет значение NULL, содержимое параметра  _lpcValues_ — ноль. 
    
 _lppPropArray_
  
> [out] Указатель на указатель на полученные значения свойств.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Значения свойств были успешно извлечены.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов в целом был успешным, но не удалось получить доступ к одному или более свойствам. Член **aulPropTag** значения свойства для каждого недоступного свойства имеет тип свойства PT_ERROR идентификатора 0. При возвращении этого предупреждения вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **макрос** HR_FAILED. Дополнительные сведения см. в [теме "Использование макроса для обработки ошибок".](using-macros-for-error-handling.md)
    
MAPI_E_INVALID_PARAMETER 
  
> Ноль был передан в **члене cValues** структуры **SPropTagArray,** на который указывает _lpPropTagArray._
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp::GetProps** получает значения свойств одного или более свойств объекта. 
  
Значения свойств возвращаются в том же порядке, в который они были запрощены (то есть порядок свойств в массиве тегов свойств, на который указывает _lpPropTagArray,_ соответствует порядку в массиве структур значений свойств, на которые указывает _lppPropArray)._ 
  
Типы свойств, указанные в членах **aulPropTag** массива тегов свойств, указывают тип значения, которое должно быть возвращено в члене **Value** каждой структуры значений свойств. Однако если вызываемая часть не знает тип свойства, вместо этого можно установить тип в члене **aulPropTag** PT_UNSPECIFIED. При искомом значении **GetProps** задает правильный тип в члене **aulPropTag** структуры значения свойства. 
  
Если типы свойств указаны в **объекте SPropTagArray** в  _lpPropTagArray,_ значения свойств **в объекте SPropValue,** возвращаемом  _в lppPropArray,_ имеют типы, которые точно соответствуют запрашиваемым типам, если только не возвращается значение ошибки. 
  
Строковые свойства могут иметь один из двух типов свойств: PT_UNICODE для представления формата Юникод и PT_STRING8 для представления формата ANSI. Если флаг MAPI_UNICODE задан в параметре  _ulFlags,_ каждый раз, когда **GetProps** не удается определить подходящий формат для строки свойства, он возвращает его значение в формате Юникод. **GetProps** не может определить точный тип строки свойства в следующих ситуациях: 
  
- Для  _параметра lpPropTagArray_ задано NULL для запроса всех свойств. 
    
- Член **aulPropTag** включает значение, PT_UNSPECIFIED в виде типа свойства в массиве тегов свойств. 
    
Если для  _параметра lpPropTagArray_ задано NULL для получения всех свойств объекта, а свойства не существуют, **GetProps** делает следующее: 
  
- Возвращает S_OK.
    
- Задает для значения подсчета в **члене cValues** структуры значений свойства значение 0. 
    
- Устанавливает для содержимого  _lpcValues_ 0. 
    
- Устанавливает _для lppPropArray nULL._ 
    
 **GetProps** не должен возвращать свойства с несколькими значениями, для **значений cValue установлено** значение 0. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вызовите [функцию MAPIAllocateBuffer,](mapiallocatebuffer.md) чтобы изначально выделить память для [структуры SPropValue,](spropvalue.md) на который указывает  _lpPropTagArray;_ вызовите [MAPIAllocateMore,](mapiallocatemore.md) чтобы выделить дополнительную память, необходимую для членов структуры. 
  
Возвращает MAPI_W_ERRORS_RETURNED, если не удается получить значение одного или более из запрашиваемого свойства. В структуре значений свойства установите для типа в члене **aulPropTag** значение PT_ERROR и значение в код состояния, описывая ошибку.  Например, если необходимо преобразовать строку в Юникод и не  поддерживать Юникод, установите для MAPI_E_BAD_CHARWIDTH. Если свойство слишком большое, установите для него MAPI_E_NOT_ENOUGH_MEMORY. Если объект не поддерживает свойство, установите для него MAPI_E_NOT_FOUND. 
  
Реализация метода **GetProps** удаленного поставщика транспорта должна возвращать значения свойств папки для свойств, запрашиваемого вызываемой программой. Реализация должна сделать следующее: 
  
- Вы можете выделить массив значений свойств для возврата вызываемой цели и сохранить его адрес в параметре указателя значения свойства, переданном для этой цели.
    
- Скопируйте теги свойств из свойств папки в теги свойств в массиве значений свойств в соответствии с массивом тегов свойств, переданных **в GetProps.**
    
- Убедитесь, что для всех тегов свойств, переданных **в GetProps,** установлен тип свойства. Вызываемая может передать тип свойства PT_UNSPECIFIED, в этом случае **GetProps** должен установить правильный тип свойства для этого тега свойства. 
    
- Установите значение каждого свойства в массиве значений свойств в соответствии с его тегом. Например, если запрашивается тег свойства **PR_OBJECT_TYPE** ([PidTagObjectType),](pidtagobjecttype-canonical-property.md) **GetProps** может установить значение MAPI_FOLDER. 
    
- Если вызываемая передает какие-либо теги свойств, которые не обрабатываются реализацией, можно установить для тега свойства значение PT_ERROR для этих свойств и установить значение свойства MAPI_E_NOT_FOUND.
    
- Возвращает S_OK, если ошибок не было или MAPI_W_ERRORS_RETURNED ошибки.
    
Реализация метода **GetProps** удаленного поставщика транспорта должна поддерживать как минимум следующие свойства: 
  
- **PR_ACCESS** ([PidTagAccess)](pidtagaccess-canonical-property.md)
    
- **PR_ACCESS_LEVEL** ([PidTagAccessLevel)](pidtagaccesslevel-canonical-property.md)
    
- **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount)](pidtagassociatedcontentcount-canonical-property.md)
    
- **PR_CONTENT_COUNT** ([PidTagContentCount)](pidtagcontentcount-canonical-property.md)
    
- **PR_CREATION_TIME** ([PidTagCreationTime)](pidtagcreationtime-canonical-property.md)
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)
    
- **PR_FOLDER_TYPE** ([PidTagFolderType)](pidtagfoldertype-canonical-property.md)
    
- **PR_OBJECT_TYPE**
    
- **PR_SUBFOLDERS** ([PidTagSubfolders)](pidtagsubfolders-canonical-property.md)
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Для свойств типа PT_OBJECT вызвать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) вместо **GetProps.** 
  
Для безопасных свойств не следует рассчитывать на их извлечение путем вызова **GetProps** с параметром  _lppPropTagArray,_ установленным в NULL. При вызове **GetProps** необходимо явно установить идентификатор безопасного свойства в члене **aulPropTag** массива тегов свойств. Когда и как доступно безопасное свойство, может быть только у поставщика услуг. 
  
Освободите возвращенную **структуру SPropValue,** вызывая функцию [MAPIFreeBuffer,](mapifreebuffer.md) только если **GetProps** возвращает S_OK или MAPI_W_ERRORS_RETURNED. 
  
Если **GetProps** возвращает MAPI_W_ERRORS_RETURNED из-за того, что ему не удалось получить доступ к одному или более свойствам, проверьте теги свойств возвращенных свойств. В структуре значений свойств сбойных свойств будет иметь следующие значения: 
  
- Тип свойства в члене **aulPropTag** имеет PT_ERROR. 
    
- Значение свойства в члене **Value** имеет код состояния для ошибки, например MAPI_E_NOT_FOUND. 
    
Свойства, которые не удается, так как они слишком большие, чтобы  удобно возвращаться в структуре значения свойства, имеют значение MAPI_E_NOT_ENOUGH_MEMORY. Обычно это происходит со строками или двоичными свойствами типа PT_STRING8, PT_UNICODE или PT_BINARY, если значение свойства составляет 4 КБ или больше. Вызовите **IMAPIProp::OpenProperty,** чтобы получить большие свойства. 
  
Не все реализации **GetProps** поддерживают форматы Юникода и ANSI для строк символов. Если определенному свойству требуется преобразование формата строки  и **GetProps** не может его поддерживать, для значения свойства устанавливается значение MAPI_E_BAD_CHARWIDTH. 
  
Чтобы проверить, является ли PST-объектом SharePoint, необходимо установить PST с помощью [IMAPISession::OpenMsgStore,](imapisession-openmsgstore.md)а затем вызвать **GetProps** на объекте хранилищ сообщений, запрашивающих это свойство. Если он существует, можно предположить, что PST настроен для SharePoint; В этом случае PST не был настроен в качестве PST-службы SharePoint. 
  
Дополнительные сведения об использовании **GetProps** для доступа к свойствам см. в подзапуске свойств [MAPI.](retrieving-mapi-properties.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI использует метод **IMAPIProp::GetProps** для получения всех свойств объекта путем передачи NULL или массива, возвращаемого методом [IMAPIProp::GetPropList](imapiprop-getproplist.md) в параметре _lpPropTagArray._  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Искомые свойства MAPI](retrieving-mapi-properties.md)
  
[Использование макроса для обработки ошибок](using-macros-for-error-handling.md)

