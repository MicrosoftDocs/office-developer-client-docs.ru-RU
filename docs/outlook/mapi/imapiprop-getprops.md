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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Извлекает значение свойства одного или более свойств объекта.
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a>Parameters

 _lpPropTagArray_
  
> [in] Указатель на массив тегов свойств, которые определяют свойства, значения которых должны быть извлечены. Параметр  _lpPropTagArray_ должен быть либо NULL, указывающее, что значения для всех свойств объекта должны быть возвращены, либо указать на структуру [SPropTagArray,](sproptagarray.md) которая содержит один или несколько тегов свойств. 
    
 _ulFlags_
  
> [in] Битмаска флагов, которая указывает формат свойств, которые имеют тип PT_UNSPECIFIED. Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Значения строк для этих свойств должны быть возвращены в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки должны быть возвращены в формате ANSI.
    
 _lpcValues_
  
> [вышел] Указатель на количество значений свойств, на которые указывает параметр _lppPropArray._ Если  _lppPropArray_ является NULL, содержимое  _параметра lpcValues_ нулевое. 
    
 _lppPropArray_
  
> [вышел] Указатель на указатель на извлеченные значения свойства.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Значения свойств были успешно извлечены.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов удался в целом, но не удалось получить доступ к одному или более свойствам. Член **aulPropTag** значения свойства для каждого недоступного свойства имеет тип свойства PT_ERROR и идентификатор нуля. Когда это предупреждение возвращается, вызов должен быть обработан как успешный. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения см. в [дополнительных сведениях Об использовании макроса для обработки ошибок.](using-macros-for-error-handling.md)
    
MAPI_E_INVALID_PARAMETER 
  
> Zero передается в **члене cValues** структуры **SPropTagArray,** на который указывает _lpPropTagArray._
    
## <a name="remarks"></a>Примечания

Метод **IMAPIProp::GetProps** получает значения свойств одного или более свойств объекта. 
  
Значения свойств возвращаются в том же порядке, что и запрашивалось (то есть порядок свойств в массиве тегов свойств, на которые указывает _lpPropTagArray,_ соответствует порядку в массиве структур значений свойств, на которые указывает _lppPropArray)._ 
  
Типы свойств, указанные в **aulPropTag** в массиве тегов свойств, указывают тип значения, которое должно быть возвращено в члене **значения** каждой структуры значения свойства. Однако если вызываемая не знает тип свойства, тип в **члене aulPropTag** можно установить вместо PT_UNSPECIFIED. При ирисовке значения **GetProps** задает правильный тип в **члене aulPropTag** структуры значения свойства для свойства. 
  
Если типы свойств указаны в **SPropTagArray** в  _lpPropTagArray,_ значения свойств в **SPropValue,** возвращаемом  _в lppPropArray,_ имеют типы, которые точно соответствуют запрашиваемым типам, если вместо этого не будет возвращено значение ошибки. 
  
Свойства string могут иметь один из двух типов свойств: PT_UNICODE для представления формата Юникод и PT_STRING8 для представления формата ANSI. Если флаг MAPI_UNICODE задан в параметре  _ulFlags,_ каждый раз, когда **GetProps** не может определить подходящий формат для свойства строки, он возвращает его значение в формате Unicode. **GetProps** не может определить точный тип свойства строки в следующих ситуациях: 
  
- Параметр  _lpPropTagArray_ задан nULL для запроса всех свойств. 
    
- Член **aulPropTag** включает значение PT_UNSPECIFIED как тип свойства в массиве тегов свойств. 
    
Если параметр  _lpPropTagArray_ задан nULL для получения всех свойств объекта и не существует свойств, **GetProps** делает следующее: 
  
- Возвращает S_OK.
    
- Задает значение отсчета в **члене cValues** структуры значения свойства до 0. 
    
- Задает содержимое  _lpcValues_ до 0. 
    
- Задает  _lppPropArray_ в NULL. 
    
 **GetProps** не должен возвращать свойства с несколькими значениями **с набором cValues** до 0. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вызов [функции MAPIAllocateBuffer](mapiallocatebuffer.md) для выделения памяти изначально для [структуры SPropValue,](spropvalue.md) на которые указывает  _lpPropTagArray;_ вызов [MAPIAllocateMore,](mapiallocatemore.md) чтобы выделить дополнительную память, необходимую для членов структуры. 
  
Возврат MAPI_W_ERRORS_RETURNED, если вы не можете получить значение для одного или более запрашиваемого свойства. В структуре значения свойства установите тип в члене **aulPropTag** для PT_ERROR и участника **Value** к коду состояния, который описывает ошибку. Например, если вам необходимо преобразовать строку в Unicode и не поддерживать Юникод, установите для участника **Value** значение MAPI_E_BAD_CHARWIDTH. Если свойство слишком большое, установите его MAPI_E_NOT_ENOUGH_MEMORY. Если объект не поддерживает свойство, установите его MAPI_E_NOT_FOUND. 
  
Реализация методом **GetProps** удаленного поставщика транспорта должна вернуть значения свойств папки для свойств, запрашиваемого вызываемой вызываемой. Реализация должна сделать следующее: 
  
- Выделим массив значений свойств, чтобы вернуться к вызываемой и сохранить его адрес в параметре указателя значения свойства, переданного для этой цели.
    
- Скопируйте теги свойств из свойств папки в теги свойств в массиве значений свойства в соответствии с массивом тегов свойств, переданных **GetProps.**
    
- Убедитесь, что тип свойства установлен для всех тегов свойств, переданных **GetProps.** Вызываемая может передаваться в типе свойства PT_UNSPECIFIED, в этом случае **GetProps** должен задать правильный тип свойства для этого тега свойства. 
    
- Установите значение каждого свойства в массиве значений свойства в соответствии с его тегом. Например, если тег свойства, запрашиваемого  звонивцом, PR_OBJECT_TYPE [(PidTagObjectType),](pidtagobjecttype-canonical-property.md) **GetProps** может задать значение MAPI_FOLDER. 
    
- Если звонивка передает в теги свойств, которые не обрабатываются реализацией, можно установить тег свойства PT_ERROR для этих свойств и установить значение свойства MAPI_E_NOT_FOUND.
    
- Возврат S_OK, если ошибки не произошли или MAPI_W_ERRORS_RETURNED если были ошибки.
    
Реализация метода **GetProps** для удаленного поставщика транспорта должна как минимум поддерживать следующие свойства: 
  
- **PR_ACCESS** [(PidTagAccess)](pidtagaccess-canonical-property.md)
    
- **PR_ACCESS_LEVEL** [(PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))
    
- **PR_ASSOC_CONTENT_COUNT** [(PidTagAssociatedContentCount)](pidtagassociatedcontentcount-canonical-property.md)
    
- **PR_CONTENT_COUNT** [(PidTagContentCount)](pidtagcontentcount-canonical-property.md)
    
- **PR_CREATION_TIME** [(PidTagCreationTime)](pidtagcreationtime-canonical-property.md)
    
- **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
    
- **PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)
    
- **PR_FOLDER_TYPE** [(PidTagFolderType)](pidtagfoldertype-canonical-property.md)
    
- **PR_OBJECT_TYPE**
    
- **PR_SUBFOLDERS** [(PidTagSubfolders)](pidtagsubfolders-canonical-property.md)
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Для свойств типа PT_OBJECT вызываем [метод IMAPIProp::OpenProperty](imapiprop-openproperty.md) вместо **GetProps.** 
  
Для безопасных свойств не ожидайте их получения, позвонив **в GetProps** с параметром  _lppPropTagArray,_ заданным nULL. При вызове **GetProps** необходимо явно установить идентификатор защищенного свойства в **члене aulPropTag** массива тегов свойств. Когда и как доступно безопасное свойство, до поставщика услуг. 
  
Освободите возвращенную **структуру SPropValue,** позвонив функции [MAPIFreeBuffer](mapifreebuffer.md) только в том случае, если **GetProps** S_OK или MAPI_W_ERRORS_RETURNED. 
  
Если **GetProps** возвращает MAPI_W_ERRORS_RETURNED из-за того, что он не может получить доступ к одному или более свойствам, проверьте теги свойств возвращенных свойств. В структуре значения свойства сбойными свойствами будут задатки следующих значений: 
  
- Тип свойства в **члене aulPropTag,** замещенный PT_ERROR. 
    
- Значение свойства в **члене Value** за набором кода состояния для ошибки, например MAPI_E_NOT_FOUND. 
    
Свойства, которые не удается, так как они слишком большие, чтобы  удобно возвращаться в структуре значения свойства, имеют свой член значения, MAPI_E_NOT_ENOUGH_MEMORY. Как правило, это происходит со строками или двоичными свойствами типа PT_STRING8, PT_UNICODE или PT_BINARY, когда значение свойства 4 КБ или больше. Вызов **IMAPIProp::OpenProperty для** получения больших свойств. 
  
Не все реализации **GetProps** поддерживают форматы Unicode и ANSI для строк символов. Если для определенного свойства требуется преобразование формата строки и **GetProps** не может его поддерживать, значение для свойства заданной MAPI_E_BAD_CHARWIDTH.  
  
Чтобы проверить, является ли PST SharePoint PST, смонтировать PST с помощью [IMAPISession::OpenMsgStore,](imapisession-openmsgstore.md)а затем вызвать **GetProps** на объекте магазина сообщений с запросом этого свойства. Если он существует, можно предположить, что PST был настроен для SharePoint; если нет, PST не был настроен как SharePoint PST. 
  
Дополнительные сведения об использовании **GetProps** для доступа к свойствам см. в дополнительных сведениях о том, как получить доступ к [свойствам MAPI.](retrieving-mapi-properties.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI использует метод **IMAPIProp::GetProps** для получения всех свойств объекта путем передачи NULL или массива, возвращенного методом [IMAPIProp::GetPropList](imapiprop-getproplist.md) в параметре _lpPropTagArray._  <br/> |
   
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
  
[Ирисовка свойств MAPI](retrieving-mapi-properties.md)
  
[Использование макроса для обработки ошибок](using-macros-for-error-handling.md)

