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
ms.openlocfilehash: 88b6f220f812f419b3f881aaa7f70a22186b589e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563802"
---
# <a name="imapicontainergethierarchytable"></a>IMAPIContainer::GetHierarchyTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель на таблицу иерархии контейнера.
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как возвращается информация в таблице. Можно задать следующие флажки:
    
CONVENIENT_DEPTH 
  
> Заполнение таблицы иерархии контейнеров из нескольких уровней. Если CONVENIENT_DEPTH не установлен, в таблице иерархии содержит только дочерних контейнеров контейнера.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** может вернуть успешно, возможно перед таблице можно сделать доступной для вызывающего абонента. Если в таблице не поддерживается, вызов последующие таблицы может вызвать ошибку. 
    
MAPI_UNICODE 
  
> Запросы, которые столбцы, которые содержат строковые данные возвращаются в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки должны возвращаться в формате ANSI. 
    
SHOW_SOFT_DELETES
  
> Отображает элементы, которые в настоящее время помечены как программных удалены, то есть, они находятся в хранения удаленных элементов этап времени.
    
 _lppTable_
  
> [out] Указатель на указатель на таблицу иерархии.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> В таблице иерархии был успешно извлечен.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.
    
MAPI_E_NO_SUPPORT 
  
> Контейнер имеет нет дочерних контейнеров и не могут предоставить таблицы иерархии.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIContainer::GetHierarchyTable** возвращает указатель в таблице иерархии контейнера. Таблица иерархии содержит сводную информацию о дочерних контейнеров в контейнере. Таблиц иерархии папок хранения сведений о вложенных папок; таблиц иерархии адресной книги хранения сведений о дочерних контейнеров адресной книги и списки рассылки. 
  
Существует возможность для некоторых контейнеров иметь нет дочерних контейнеров. Эти контейнеры возврата MAPI_E_NO_SUPPORT из их реализации **GetHierarchyTable**.
  
Если флаг CONVENIENT_DEPTH, каждой строки в таблице иерархии также включает свойство **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) в столбце. **PR_DEPTH** уровень каждого контейнера относительно контейнера, который реализует таблицы. Реализации контейнер дочерних контейнеров выглядят с глубиной нулю, дочерних контейнеров в ноль глубины контейнеров, число уровней в одно и т. д. Последовательная увеличения значения **PR_DEPTH** как deepens иерархию уровней. 
  
Полный список обязательные и дополнительные столбцы в таблицах иерархии [Таблиц иерархии](hierarchy-tables.md)см.
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Если вы поддерживаете таблицы иерархии для контейнера, необходимо выполнить следующее:
  
- Поддерживает вызов метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера для открытия свойство **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).
    
- Возвращает **PR_CONTAINER_HIERARCHY** в вызове методов [IMAPIProp::GetPropList](imapiprop-getproplist.md) или [IMAPIProp::GetProps](imapiprop-getprops.md) контейнера. 
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Строка и двоичный столбцов таблицы содержимое может быть усечен. Как правило поставщики возвращать 255 символов. Так как не известно, заранее ли таблицы включает в себя усеченных столбцы, предполагается, что столбец усекается, если длина столбца — 255 или 510 байт. Всегда можно будет извлечь полное значение усеченных столбца, при необходимости непосредственно из объекта с помощью его идентификатор записи чтобы его открыть, затем вызвать метод [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
В зависимости от реализации поставщика, ограничения и операции сортировки можно применять к строку целиком или усеченных версии этой строки. Кроме того поставщики хранилища не обязательно соблюдать набор порядок сортировки, который [SSortOrderSet](ssortorderset.md) , указанный для таблиц иерархии. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |Класс CHierarchyTableTreeCtrl **GetHierarchyTable** используется для получения таблиц иерархии для отображения в элементе управления дерева.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Каноническое свойство PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

