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
ms.openlocfilehash: 462d42d68bddba72fd81b97e2aeb9eb5ee8c9c20
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588008"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Получает значение свойства из одного или нескольких свойств объекта.
  
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
  
> [in] Указатель на массив тегов свойств, чтобы указать свойства, значения которых нужно вернуть. Параметр _lpPropTagArray_ должен иметь значение NULL, указывающее, что значения всех свойств объекта должны быть возвращены, укажите на структуру [SPropTagArray](sproptagarray.md) , содержит один или несколько тегов свойств. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, которое указывает формат для свойства, имеющие тип PT_UNSPECIFIED. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Строковые значения для этих свойств должны возвращаться в формате Юникод. Если флаг MAPI_UNICODE не установлен, строковые значения должны возвращаться в формате ANSI.
    
 _lpcValues_
  
> [out] Указатель на количество значений свойств, на который указывает параметр _lppPropArray_ . Если _lppPropArray_ имеет значение NULL, содержимое параметра _lpcValues_ равно нулю. 
    
 _lppPropArray_
  
> [out] Указатель на указатель на извлеченное свойство значения.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Значения свойств были успешно извлечен.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов завершился успешно в целом, но не удается получить доступ к одного или нескольких свойств. Член **aulPropTag** значение свойства для каждого свойства, недоступен имеет тип свойства PT_ERROR и идентификатора нулю. При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).
    
MAPI_E_INVALID_PARAMETER 
  
> Член **cValues** структуры **SPropTagArray** , на который указывает _lpPropTagArray_был передан нулю.
    
## <a name="remarks"></a>Замечания

Метод **IMAPIProp::GetProps** получает значения свойств из одного или нескольких свойств объекта. 
  
Значения свойств возвращаются в том же порядке, как они были запрошено (то есть, порядок свойств в массиве свойство tag указывает соответствия _lpPropTagArray_ порядке в массиве структур значение свойства указывает _lppPropArray _). 
  
Типы свойств, указанных в **aulPropTag** элементы массива тега свойства указывают тип значение, которое должны быть возвращены в элемент **значения** структуры значение каждого свойства. Тем не менее если вызывающий не имеет тип свойства, типа в элемент **aulPropTag** может быть присвоено вместо PT_UNSPECIFIED. При получении значение **GetProps** задает правильный тип в член **aulPropTag** структуры значение свойства для свойства. 
  
Если типы свойств заданы в **SPropTagArray** в _lpPropTagArray_, значения свойств в **SPropValue** , возвращаемых в _lppPropArray_ типами, точно соответствовать запрошенных типов, если не возвращаемое значение ошибки Вместо этого. 
  
Свойства строка может иметь одно из двух типов свойств: PT_UNICODE для представления формата Юникод и PT_STRING8 для представления формата ANSI. Если флаг MAPI_UNICODE установлен в параметре _ulFlags_ каждый раз, когда **GetProps** не может определить соответствующий формат для свойства строки, возвращается его значение в формате Юникод. **GetProps** не может определить тип свойства точной строки в следующих ситуациях: 
  
- Параметр _lpPropTagArray_ задано значение NULL, чтобы запросить все свойства. 
    
- Член **aulPropTag** содержит значение PT_UNSPECIFIED в качестве свойства типа в массиве тега свойства. 
    
Если параметр _lpPropTagArray_ задано значение NULL для извлечения всех свойств объекта, а свойства не существует, **GetProps** выполняет следующие действия. 
  
- Возвращает значение S_OK.
    
- Задает значение числа в член **cValues** структуры свойство значение 0. 
    
- Задает содержимое _lpcValues_ 0. 
    
- Задает _lppPropArray_ значение NULL. 
    
 **GetProps** не должен возвращать, что свойства с несколькими значениями с **cValues** значение 0. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Вызовите функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) изначально выделить память для структуры [SPropValue](spropvalue.md) , на который указывает _lpPropTagArray_; вызов [MAPIAllocateMore](mapiallocatemore.md) распределения любой дополнительной памяти, необходимый для членов структуры. 
  
Возвращает MAPI_W_ERRORS_RETURNED, если вы не сможете получить значение для одного или нескольких запрошенных свойств. В структуре значение свойства установите тип в **aulPropTag** к PT_ERROR, а **значение** код состояния, с описанием ошибки. Например если для преобразования строки Юникод и не поддерживает Юникод, установите **значение** равным MAPI_E_BAD_CHARWIDTH. Если свойство имеет слишком большой, задайте значение MAPI_E_NOT_ENOUGH_MEMORY. Если объект не поддерживает свойство, присвойте этому параметру MAPI_E_NOT_FOUND. 
  
Реализация поставщика транспорта удаленного метода **GetProps** должен возвращать значения свойств папки для запрошенного вызывающим абонентом. Внедрения необходимо выполнить следующие действия. 
  
- Выделите массив значений свойство вернуться к вызывающему и сохранить его адрес с помощью параметра указатель значение свойства переданную для этой цели.
    
- Копирование свойств папки тегов свойств в свойство теги в массиве значение свойства в соответствии с массива тегов свойств, переданной в **GetProps**.
    
- Убедитесь, что тип свойства для всех свойств тегов, переданной в **GetProps**. В свойство типа PT_UNSPECIFIED, в котором case **GetProps** необходимо установить правильный тип для этого свойства тега должно пройти вызывающего абонента. 
    
- Задайте значение каждого свойства в массиве значение свойства в соответствии с его тег. Например если свойство тег, запрошенную вызывающим **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** можно задать значение MAPI_FOLDER. 
    
- Вызывающего абонента передает все теги свойства, которые не работают внедрения, можно установите свойство tag PT_ERROR для этих свойств и задайте для свойства значение MAPI_E_NOT_FOUND.
    
- Возвращает значение S_OK, если ошибок не или MAPI_W_ERRORS_RETURNED при наличии ошибок.
    
Реализация поставщика транспорта удаленного метода **GetProps** должен поддерживать по крайней мере следующие свойства: 
  
- **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))
    
- **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))
    
- **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_OBJECT_TYPE**
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Для свойства типа PT_OBJECT вызовите метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) вместо **GetProps**. 
  
Для свойства безопасности не ожидается их извлечь путем вызова **GetProps** с параметром _lppPropTagArray_ задано значение NULL. Явным образом, необходимо установить идентификатор secure свойства в **aulPropTag** членом массива тег его свойства при вызове **GetProps**. Когда и как безопасной свойство доступно зависит от поставщика услуг. 
  
Бесплатная загрузка возвращенные структура **SPropValue** путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) только в том случае, если **GetProps** возвращает значение S_OK или MAPI_W_ERRORS_RETURNED. 
  
Если **GetProps** возвращает MAPI_W_ERRORS_RETURNED, так как он не удалось получить доступ к одной или нескольких свойств, проверьте свойство теги возвращаемых свойств. Сбой свойств будет иметь следующие значения, заданные в их структуру значение свойства: 
  
- Тип свойства в **aulPropTag** набор элементов для PT_ERROR. 
    
- Код состояния для ошибки, такие как MAPI_E_NOT_FOUND принимает значение свойства в элемент **значения** . 
    
Свойства, завершившихся неудачно из-за слишком большого легко создавать будут возвращаться в структуре значение свойства имеют их **значение** набор элементов в MAPI_E_NOT_ENOUGH_MEMORY. Обычно это происходит с строку или двоичный свойств типа PT_STRING8, PT_UNICODE или PT_BINARY Если значение свойства 4 КБ или больше. Вызов **IMAPIProp::OpenProperty** для извлечения больших свойства. 
  
Не все реализации **GetProps** поддерживает форматы ANSI и Юникод для строк. Когда определенное свойство требует преобразования формата строки и **GetProps** не поддерживает ее, элемент **значение** для свойства имеет значение MAPI_E_BAD_CHARWIDTH. 
  
Чтобы проверить, является ли файл личных ПАПОК SharePoint PST, подключите PST-файлов с помощью [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), затем вызвать **GetProps** объекта хранилища сообщений, запрашивающего это свойство. Если он существует, можно предположить, что PST-файлов будет настроен для SharePoint; в противном случае PST не был настроен как SharePoint PST. 
  
Дополнительные сведения об использовании **GetProps** для доступа к свойствам можно [Извлечение свойств MAPI](retrieving-mapi-properties.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |Mfcmapi (en) использует метод **IMAPIProp::GetProps** для получения всех свойств для объекта, передавая NULL или массива, возвращенных методом [IMAPIProp::GetPropList](imapiprop-getproplist.md) с помощью параметра _lpPropTagArray_ .  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Извлечение свойств MAPI](retrieving-mapi-properties.md)
  
[Обработка ошибок с помощью макросов](using-macros-for-error-handling.md)

