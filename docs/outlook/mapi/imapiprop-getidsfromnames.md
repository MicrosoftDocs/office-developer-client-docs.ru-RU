---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5247ca71c88b9c0f8591a732746a17204265741c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809037"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**Относится к**: Outlook 
  
Предоставляет свойство идентификаторы, соответствующие имена одного или нескольких свойств.
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a>Параметры

 _cPropNames_
  
> [in] Count имена свойств, на который указывает параметр _lppPropNames_ . Если _lppPropNames_ имеет значение NULL, параметр _cPropNames_ должен иметь значение 0. 
    
 _lppPropNames_
  
> [in] Указатель на массив имена свойств, или значение NULL. Передача значение NULL, запрашивает идентификаторы свойств в все наборы свойств о том, какие объект содержит сведения о всех имен свойств. Параметр _lppPropNames_ не должна быть NULL, если флаг MAPI_CREATE установлен в параметре _ulFlags_ . 
    
 _ulFlags_
  
> [in] Битовая маска флаги, которое указывает, как должны быть возвращены идентификаторы свойств. Можно задать следующий флаг:
    
MAPI_CREATE 
  
> Если один не еще не присвоен, к одному или нескольким имена, включенные в массиве имя свойства, на который указывает _lppPropNames_, назначает идентификатор свойства. Этот флаг не зарегистрирует идентификатор в таблице сопоставления идентификатор имени.
    
 _lppPropTags_
  
> [out] Указатель на указатель на массив тегов свойств, содержащий существующие или новые назначенные идентификаторы свойств. Типы свойств для тегов свойств этого массива устанавливаются **PT_UNSPECIFIED**.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Идентификаторы для указанного свойства имена были успешно возвращен.
    
MAPI_E_NO_SUPPORT 
  
> Объект не поддерживает именованные свойства.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Недостаточно памяти была доступна для получения идентификаторов.
    
MAPI_E_TOO_BIG 
  
> Операцию не удается выполнить из-за слишком большого числа тегов свойства которого требуется получить.
    
MAPI_W_ERRORS_RETURNED 
  
> Вызов завершился успешно в целом, но не должны возвращаться один или несколько идентификаторов свойств. Соответствующий тип свойства для каждого свойства, недоступен — это значение **PT_ERROR** и его идентификатор нулевое значение. При возвращении этого предупреждения обработки вызова как успешно. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. В разделе [Использование макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Замечания

Метод **IMAPIProp::GetIDsFromNames** получает массив теги свойства, в которых содержатся идентификаторы свойств для одного или нескольких именованных свойств. **IMAPIProp::GetIDsFromNames** могут вызываться для выполнения следующих: 
  
- Создайте идентификаторы для новых имен.
    
- Получите идентификаторы для определенных имен.
    
- Получите идентификаторы для всех именованных свойств, которые включены в объект сопоставления.
    
Именованные свойства обычно используются поставщиками хранилища сообщений для сообщений и папок. Другие объекты, таких как системы обмена сообщениями разделах профилей и пользователи могут не поддерживать связь имена идентификаторов свойств и может возвращать MAPI_E_NO_SUPPORT из **GetIDsFromNames**.
  
Если ошибка, которая возвращает идентификатор для определенного имени, **GetIDsFromNames** MAPI_W_ERRORS_RETURNED возвращает и задает тип свойства в строке массива свойства tag, соответствующий имени **PT_ERROR** и идентификатор нулевое значение. 
  
Идентификатор имени сопоставление представлено свойством объекта **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)). **PR_MAPPING_SIGNATURE** содержит структуру [MAPIUID](mapiuid.md) , которое указывает, ответственного за объект поставщика услуг. Если свойство **PR_MAPPING_SIGNATURE** является общим для двух объектов, предполагают, что эти объекты используют то же сопоставление идентификатор имени. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Идентификаторы, передается обратно в массиве тег свойство указывает параметр _lppPropNames_ должен быть в диапазоне 0x8000 для 0xFFFE. Записи в этот массив должен быть в том же порядке, как имена, переданные в массиве имя свойства указывает _lppPropNames_. 
  
Если вы поддерживаете именованных свойств в контейнере, используйте одно сопоставление идентификатор имени для всех объектов в контейнере (то есть, не используйте разные сопоставления для каждой папке в хранилище сообщений или каждого сообщения в папке).
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Так как типы свойств, возвращенный идентификаторов в массиве тег свойства, на который указывает _lppPropTags_ **PT_UNSPECIFIED**, необходимо вызвать метод [IMAPIProp::SetProps](imapiprop-setprops.md) для извлечения точных типов. 
  
При перемещении или копировать объекты с именованного свойства и объекты источника и назначения имеют различные сопоставления подписи, как указано в значения свойств своих **PR_MAPPING_SIGNATURE** , должны сохранить имена при выполнении этих операций. Чтобы сохранить имена свойств, настройте соответствующие идентификаторы свойства в соответствии с сопоставлением идентификатор имени конечного объекта. 
  
Некоторые объекты настроено ограничение на число идентификаторов свойств, которые можно присвоить имя. Если вызов **GetIDsFromNames** вызывает превышение этого ограничения, метод возвращает MAPI_E_TOO_BIG. В этом случае запроса по идентификатору. 
  
Для получения дополнительных сведений см [MAPI с именем свойства](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedPropsUsed  <br/> |Mfcmapi (en) использует метод **IMAPIProp::GetIDsFromNames** для получения теги свойства для всех именованных свойств, которые были сопоставлены.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Именованные свойства MAPI](mapi-named-properties.md)
  
[Обработка ошибок с помощью макросов](using-macros-for-error-handling.md)
