---
title: IMAPISupportModifyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4c296b12d2dc98c4ff8d94349298e9dda0fb9409
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419991"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Вносит изменения в раздел профиля хранения сообщений без изменений.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] Битоваяmas флагов, которая указывает тип хранения сообщений. Можно установить следующий флаг:
    
MDB_TEMPORARY 
  
> Хранилище сообщений является временным и не должно быть добавлено в таблицу хранения сообщений. Если MDB_TEMPORARY, **ModifyProfile** возвращает S_OK немедленно. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Изменения раздела профиля были успешно внесены.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::ModifyProfile реализован** для объектов поддержки поставщика store сообщений. Поставщики store сообщений **звонят modifyProfile,** чтобы упредить MAPI изменить данные своего профиля. 
  
 **ModifyProfile** добавляет раздел профиля, связанный с поставщиком вызовов, в список ресурсов поставщика установленного магазина сообщений. В результате хранилище сообщений отображается в таблице банка сообщений, доступной клиентам с помощью метода [IMAPISession::GetMsgStoresTable,](imapisession-getmsgstorestable.md) и открывается без отображения диалоговых окно. 
  
Если флаг MDB_TEMPORARY установлен, MAPI ничего не делает, и метод немедленно возвращается с S_OK.
  
## <a name="see-also"></a>См. также



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

