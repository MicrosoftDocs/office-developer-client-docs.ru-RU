---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c142424bb050ae287f54a87ea8a5e0ea45acb12c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411619"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает порядок сортировки по умолчанию для таблицы содержимого папки.
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpSortCriteria_
  
> [in] Указатель на структуру [SSortOrderSet,](ssortorderset.md) которая содержит порядок сортировки по умолчанию. 
    
 _ulFlags_
  
> [in] Битмашка флагов, которые контролируют, как установлен порядок сортировки по умолчанию. Можно установить следующий флаг:
    
RECURSIVE_SORT 
  
> Набор сортировки по умолчанию применяется к указанным папкам и ко всем ее подмосткам.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Порядок сортировки был успешно сохранен.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик хранения сообщений не поддерживает сохранение порядка сортировки для таблиц содержимого папок.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::SaveContentsSort** устанавливает порядок сортировки по умолчанию для таблицы содержимого папки. То есть, когда клиент вызывает метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) после вызова кода **SaveContentsSort,** строки в таблице возвращаемого контента будут отображаться в порядке, установленном **SaveContentsSort.**
  
Не все поставщики магазинов сообщений поддерживают **SaveContentsSort;** допустимо, чтобы поставщики хранения сообщений возвращали MAPI_E_NO_SUPPORT из **метода SaveContentsSort.** 
  
## <a name="see-also"></a>См. также



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

