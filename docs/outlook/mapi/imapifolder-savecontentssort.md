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
ms.openlocfilehash: 1f79265c4356747e64aa8102dd4486db229baf5a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579664"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает порядок сортировки по умолчанию для папки содержимое таблицы.
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpSortCriteria_
  
> [in] Указатель на структуру [SSortOrderSet](ssortorderset.md) , содержащий порядок сортировки по умолчанию. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как задать порядок сортировки по умолчанию. Можно задать следующий флаг:
    
RECURSIVE_SORT 
  
> Набор порядок сортировки по умолчанию применяется для указанной папки и все вложенные папки.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Порядок сортировки успешно сохранен.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик хранения сообщения не поддерживает сохранение порядок сортировки для своих таблиц содержимое папки.
    
## <a name="remarks"></a>Замечания

Метод **IMAPIFolder::SaveContentsSort** устанавливает порядок сортировки по умолчанию для папки содержимое таблицы. То есть когда клиент вызывает метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) папки после код вызывает **SaveContentsSort**, строки в таблице возвращаемых содержимое отображаются в порядке, установленные **SaveContentsSort**.
  
Не все поставщики хранилища сообщений поддерживают **SaveContentsSort**; Это допустимо для поставщиков хранилища сообщений для возврата MAPI_E_NO_SUPPORT из метода **SaveContentsSort** . 
  
## <a name="see-also"></a>См. также



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

