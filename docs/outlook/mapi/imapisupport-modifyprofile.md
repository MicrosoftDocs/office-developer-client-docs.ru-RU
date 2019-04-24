---
title: Имаписуппортмодифипрофиле
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316606"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вносит изменения в раздел профиля хранилища сообщений.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, указывающая тип хранилища сообщений. Можно задать следующий флаг:
    
МДБ_ТЕМПОРАРИ 
  
> Хранилище сообщений является временным и не должно добавляться в таблицу хранения сообщений. Если задано значение МДБ_ТЕМПОРАРИ, **модифипрофиле** ВОЗВРАЩАЕТ значение S_OK немедленно. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Изменения в разделе профиля выполнены успешно.
    
## <a name="remarks"></a>Замечания

Метод **имаписуппорт:: модифипрофиле** реализован для объектов поддержки поставщика хранилища сообщений. Поставщики хранилищ сообщений вызывают **модифипрофиле** для запроса MAPI для изменения сведений о профиле. 
  
 **Модифипрофиле** добавляет раздел профиля, связанный с поставщиком вызовов, в список установленных ресурсов поставщика хранилища сообщений. Это приводит к тому, что хранилище сообщений отображается в таблице хранилища сообщений, которое доступно клиентам через метод [IMAPISession:: жетмсгсторестабле](imapisession-getmsgstorestable.md) , и его можно открыть без отображения диалогового окна. 
  
Если установлен флаг МДБ_ТЕМПОРАРИ, MAPI не выполняет никаких действий, а метод немедленно возвращает значение S_OK.
  
## <a name="see-also"></a>См. также



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

