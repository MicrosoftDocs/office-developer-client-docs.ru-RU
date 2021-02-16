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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель на таблицу иерархии контейнера.
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет тем, как информация возвращается в таблице. Можно установить следующие флаги:
    
CONVENIENT_DEPTH 
  
> Заполняет таблицу иерархии контейнерами из нескольких уровней. Если CONVENIENT_DEPTH не установлено, таблица иерархии содержит только непосредственные юные контейнеры контейнера.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** может успешно вернуться, возможно, до того, как таблица будет доступна вызываемой. Если таблица недоступна, последующий вызов таблицы может вызвать ошибку. 
    
MAPI_UNICODE 
  
> Запрашивает, чтобы столбцы, содержащие строку данных, возвращались в формате Юникод. Если флаг MAPI_UNICODE не установлен, строки должны возвращаться в формате ANSI. 
    
SHOW_SOFT_DELETES
  
> Отображает элементы, которые в настоящее время помечены как "мягко удаленные", то есть находятся на этапе хранения удаленных элементов.
    
 _lppTable_
  
> [out] Указатель на указатель на таблицу иерархии.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица иерархии успешно извлечена.
    
MAPI_E_BAD_CHARWIDTH 
  
> Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.
    
MAPI_E_NO_SUPPORT 
  
> Контейнер не имеет child containers и не может предоставить таблицу иерархии.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIContainer::GetHierarchyTable** возвращает указатель на таблицу иерархии контейнера. В таблице иерархии содержится сводная информация о child containers в контейнере. В таблицах иерархии папок есть сведения о вложенных папках; В таблицах иерархии адресных книг содержится информация о контейнерах адресных книг и списках рассылки. 
  
У некоторых контейнеров может не быть никаких child-контейнеров. Эти контейнеры MAPI_E_NO_SUPPORT из своих реализаций **GetHierarchyTable.**
  
При CONVENIENT_DEPTH флага каждая строка в таблице иерархии также включает свойство **PR_DEPTH** ([PidTagDepth)](pidtagdepth-canonical-property.md)в качестве столбца. **PR_DEPTH** указывает уровень каждого контейнера относительно контейнера, который реализует таблицу. Непосредственные потомки контейнера реализующих контейнеров находятся на нулевой глубине, контейнеры-потомки в контейнерах нулевой глубины находятся на глубине 1 и так далее. Значения PR_DEPTH **последовательно** увеличиваются по мере углубления иерархии уровней. 
  
Полный список необходимых и необязательных столбцов в таблицах иерархии см. в [статье "Таблицы иерархии".](hierarchy-tables.md)
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если вы поддерживаете таблицу иерархии для контейнера, необходимо также сделать следующее:
  
- Поддержка вызова метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) контейнера для открытия **свойства PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy).](pidtagcontainerhierarchy-canonical-property.md)
    
- Возвращает **PR_CONTAINER_HIERARCHY** из вызова методов [IMAPIProp::GetPropList](imapiprop-getproplist.md) или [IMAPIProp::GetProps](imapiprop-getprops.md) контейнера. 
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Строки и столбцы таблицы двоичного содержимого можно усечены. Обычно поставщики возвращают 255 символов. Так как вы не можете заранее узнать, содержит ли таблица усеченные столбцы, предположим, что столбец усечен, если длина столбца составляет 255 или 510 bytes. При необходимости вы всегда можете получить полное значение усеченного столбца непосредственно из объекта, используя идентификатор записи, чтобы открыть его, а затем вызывать метод [IMAPIProp::GetProps.](imapiprop-getprops.md) 
  
В зависимости от реализации поставщика ограничения и операции сортировки могут применяться к всей строке или к усеченной версии этой строки. Кроме того, не гарантируется, что поставщики магазина будут соблюдать набор [сортировки SSortOrderSet,](ssortorderset.md) указанный для таблиц иерархии. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |Класс CHierarchyTableTreeCtrl использует **GetHierarchyTable** для получения таблиц иерархии для отображения в иерархическом представлении.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Каноническое свойство PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

