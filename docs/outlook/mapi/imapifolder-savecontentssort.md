---
title: имапифолдерсавеконтентссорт
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

 _лпсорткритериа_
  
> возврата Указатель на структуру [ссортордерсет](ssortorderset.md) , которая содержит порядок сортировки по умолчанию. 
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющих, как задается порядок сортировки по умолчанию. Можно задать следующий флаг:
    
RECURSIVE_SORT 
  
> Установленный по умолчанию порядок сортировки применяется к указанной папке и ко всем вложенным папкам.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Порядок сортировки успешно сохранен.
    
MAPI_E_NO_SUPPORT 
  
> Поставщик хранилища сообщений не поддерживает сохранение порядка сортировки для таблиц содержимого папки.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIFolder:: савеконтентссорт** устанавливает порядок сортировки по умолчанию для таблицы содержимого папки. То есть когда клиент вызывает метод [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md) папки после того, как код вызывает **савеконтентссорт**, строки в таблице возвращенные содержимое будут отображаться в порядке, установленном **савеконтентссорт**.
  
Не все поставщики хранилищ сообщений поддерживают **савеконтентссорт**; поставщики хранилищ сообщений могут возвращать MAPI_E_NO_SUPPORT из метода **савеконтентссорт** . 
  
## <a name="see-also"></a>См. также



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

