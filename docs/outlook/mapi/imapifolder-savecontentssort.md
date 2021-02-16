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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает порядок сортировки по умолчанию для таблицы содержимого папки.
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpSortCriteria_
  
> [in] Указатель на структуру [SSortOrderSet,](ssortorderset.md) которая содержит порядок сортировки по умолчанию. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет порядком сортировки по умолчанию. Можно установить следующий флаг:
    
RECURSIVE_SORT 
  
> Набор порядок сортировки по умолчанию применяется к указанным папам и всем ее вложенным папок.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Порядок сортировки успешно сохранен.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик содержимого сообщений не поддерживает сохранение порядка сортировки для таблиц содержимого папки.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder::SaveContentsSort** устанавливает порядок сортировки по умолчанию для таблицы содержимого папки. То есть, когда клиент вызывает метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) папки после вызова **метода SaveContentsSort,** строки в возвращаемой таблице содержимого будут отображаться в порядке, установленном **SaveContentsSort.**
  
Не все поставщики store сообщений **поддерживают SaveContentsSort;** Допустимо, чтобы поставщики хранения сообщений возвращали MAPI_E_NO_SUPPORT из метода **SaveContentsSort.** 
  
## <a name="see-also"></a>См. также



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

