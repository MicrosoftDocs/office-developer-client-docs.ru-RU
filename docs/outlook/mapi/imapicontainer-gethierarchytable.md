---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: efc7f7a2fa703004afe361d766e0209ba40ffe46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426200"
---
# <a name="imapicontainergethierarchytable"></a>IMAPIContainer::GetHierarchyTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель в таблицу иерархии контейнера.
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют, как возвращается информация в таблице. Можно установить следующие флаги:
    
CONVENIENT_DEPTH 
  
> Заполняет таблицу иерархии контейнерами с нескольких уровней. Если CONVENIENT_DEPTH не установлено, таблица иерархии содержит только ближайшие детские контейнеры контейнера.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** может вернуться успешно, возможно, до того, как таблица будет доступна вызываемой. Если таблица недоступна, при последующем вызове таблицы может быть допущена ошибка. 
    
MAPI_UNICODE 
  
> Запрашивает, чтобы столбцы, содержащие данные строк, возвращались в формате Unicode. Если флаг MAPI_UNICODE не установлен, строки должны быть возвращены в формате ANSI. 
    
SHOW_SOFT_DELETES
  
> Показывает элементы, которые в настоящее время помечены как мягкие удаленные, то есть они находятся на этапе времени хранения удаленных элементов.
    
 _lppTable_
  
> [вышел] Указатель на указатель на таблицу иерархии.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица иерархии была успешно извлечена.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.
    
MAPI_E_NO_SUPPORT 
  
> Контейнер не имеет детских контейнеров и не может предоставить таблицу иерархии.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIContainer::GetHierarchyTable** возвращает указатель в таблицу иерархии контейнера. В таблице иерархии содержится сводная информация о детских контейнерах в контейнере. Таблицы иерархии папок вмещены сведениями о подмостках; В таблицах иерархии адресных книг содержится информация о контейнерах детских адресных книг и списках рассылки. 
  
Некоторые контейнеры могут не иметь детских контейнеров. Эти контейнеры возвращают MAPI_E_NO_SUPPORT из их реализации **GetHierarchyTable**.
  
При задав CONVENIENT_DEPTH, каждая строка в таблице иерархии также включает **свойство PR_DEPTH** [(PidTagDepth)](pidtagdepth-canonical-property.md)в качестве столбца. **PR_DEPTH** указывает уровень каждого контейнера относительно контейнера, реализуемого в таблице. Ближайшие детские контейнеры реализующихся контейнеров находятся на нулевой глубине, детские контейнеры в контейнерах с нулевой глубиной находятся на глубине один и так далее. Значения PR_DEPTH **последовательно** увеличиваются по мере углубления иерархии уровней. 
  
Полный список необходимых и необязательных столбцов в таблицах иерархии см. в [статье Таблицы иерархии.](hierarchy-tables.md)
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если вы поддерживаете таблицу иерархии для контейнера, необходимо также сделать следующее:
  
- Поддержка вызова для метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для открытия **свойства** PR_CONTAINER_HIERARCHY [(PidTagContainerHierarchy).](pidtagcontainerhierarchy-canonical-property.md)
    
- Возврат **PR_CONTAINER_HIERARCHY** из вызова в методы [IMAPIProp::GetPropList](imapiprop-getproplist.md) или [IMAPIProp::GetProps.](imapiprop-getprops.md) 
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Столбцы таблицы строк и двоичного содержимого можно усечено. Обычно поставщики возвращают 255 символов. Поскольку вы не можете заранее узнать, включает ли таблица усеченные столбцы, предположим, что столбец усечен, если длина столбца составляет 255 или 510 bytes. При необходимости вы всегда можете получить полное значение усеченного столбца непосредственно с объекта с помощью его идентификатора входа, чтобы открыть его, а затем позвонить по методу [IMAPIProp::GetProps.](imapiprop-getprops.md) 
  
В зависимости от реализации поставщика ограничения и операции сортировки могут применяться к всей строке или к усеченной версии этой строки. Кроме того, поставщики магазинов не гарантируют соблюдать набор заказов [сортировки SSortOrderSet,](ssortorderset.md) заданный для таблиц иерархии. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |Класс CHierarchyTableTreeCtrl использует **GetHierarchyTable** для получения таблиц иерархии для отображения в области управления представлением дерева.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Каноническое свойство PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

