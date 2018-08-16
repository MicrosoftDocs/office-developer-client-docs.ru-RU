---
title: IMAPITableFindRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cb777074d1657a3ee5c2f1e9f70d2b304858c1b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809209"
---
# <a name="imapitablefindrow"></a>IMAPITable::FindRow

  
  
**Относится к**: Outlook 
  
Находит следующую строку в таблице, которая соответствует определенным условиям поиска и перемещает курсор в эту строку.
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpRestriction_
  
> [in] Указатель на структуру [SRestriction](srestriction.md) , описывающий условия поиска. 
    
 _BkOrigin_
  
> [in] Закладки, идентифицирующий строку, где **FindRow** должна начинать поиск. Закладки можно создать с помощью метода [IMAPITable::CreateBookmark](imapitable-createbookmark.md) или один из следующих предварительно заданных значений может быть передан. 
    
BOOKMARK_BEGINNING 
  
> Поиск с начала таблицы. 
    
BOOKMARK_CURRENT 
  
> Выполняет поиск строки в таблице, в котором находится курсор. 
    
BOOKMARK_END 
  
> Поиск с конца таблицы. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее направление поиска. Можно задать следующий флаг:
    
DIR_BACKWARD 
  
> Выполняет поиск строки, закладки.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Операция поиска успешно.
    
MAPI_E_INVALID_BOOKMARK 
  
> Закладки с помощью параметра _BkOrigin_ является недопустимым, так как он был удален или находится за последней строки запроса. 
    
MAPI_E_NOT_FOUND 
  
> Не были найдены строки, соответствующие ограничение.
    
MAPI_W_POSITION_CHANGED
  
> Вызов завершился успешно, но закладку, используемый в операции больше не устанавливаются в той же строке, что и при его последнего использования; Если закладка не используется, он больше не в той же позиции при его создании. При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. В разделе [Использование макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Замечания

Метод **IMAPITable::FindRow** поиск первой строки в таблице в соответствии с набор условий поиска, описанного в структуре **SRestriction** указывает параметр _lpRestriction_ . 
  
Как правило **FindRow** выполняет поиск вперед из указанной закладке. Может задать поиск, чтобы переместить назад из закладки, установив флаг DIR_BACKWARD с помощью параметра _ulFlags_ . Поиск вперед начинается с текущей закладки; Поиск в обратном направлении начинается с строке до закладки. Конечным поиска — непосредственно перед первой строки найдено, которое удовлетворены ограничение. 
  
Если строка, на который указывает на закладку в параметре _BkOrigin_ более не существует в таблице и таблицы не удается установить новую позицию закладки, **FindRow** возвращает MAPI_E_INVALID_BOOKMARK. Если строка, на который указывает _BkOrigin_ больше не существует и таблицу для установки в новое положение закладки, **FindRow** возвращает MAPI_W_POSITION_CHANGED. 
  
При BOOKMARK_BEGINNING или BOOKMARK_END закладку, переданные в _BkOrigin_ **FindRow** возвращает MAPI_E_NOT_FOUND, если нет соответствующей строки не найден. Если закладка, используемые в _BkOrigin_ BOOKMARK_CURRENT, **FindRow** может вернуть MAPI_W_POSITION_CHANGED, но не MAPI_E_INVALID_BOOKMARK, поскольку всегда текущей позиции курсора. 
  
Столбец **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) свойство является обязательным для всех таблиц и всех реализациях **FindRow** , необходимых для поддержки вызовов, поиск строки на основании PR_INSTANCE_KEY. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Тип префикс поиска выполняется сервером **FindRow** полезен только поиска следует направлении организации в таблице. Для достижения необходимых поведение функции сравнения, содержится в разрешении **RELOP_GE** передается в структуре ограничение свойства должен быть те же функции сравнения, на котором основано порядок сортировки в таблице. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

**FindRow** можно использовать для поддержки прокрутки на основании строки, введенные в пользователем, особенно в списки в диалоговых окнах адрес. В этом типе прокрутки пользователей введите постепенно больше префиксы желаемую строковое значение и периодически может выдавать **FindRow** звонка для перехода к первой строке, которая соответствует префикса. Направление перескакивает курсора зависит от направление поиска установлен на выполнение. 
  
Чтобы использовать **FindRow**, необходимо установить закладку. Поиск строки может быть создано из любого закладку, включая из предварительно закладки, которое указывает текущую позицию и начала и окончания таблицы. Если большое число строк в таблице, операции поиска может быть медленно.
  
Используйте ограничение для поиска строки префикс для прокрутки следующим образом. При поиске вперед на столбец, сортировка в порядке возрастания и обратной поиска на столбец в порядке убывания передачи структуры ограничение свойства в параметр _lpRestriction_ с отношением **RELOP_GE** и соответствующей Свойство tag и префикса, с помощью **GE** формат _тега_ _префикса_. 
  
Дополнительные сведения об использовании структур ограничение для указания фильтра, обратитесь к разделу [О ограничения](about-restrictions.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |Mfcmapi (en) использует метод **IMAPITable::FindRow** для поиска строк, которые соответствуют ограничению поиска.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
