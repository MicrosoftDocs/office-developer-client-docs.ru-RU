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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вносит изменения в раздел профилей магазина сообщений навсегда.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Битмашка флагов, которая указывает тип магазина сообщений. Можно установить следующий флаг:
    
MDB_TEMPORARY 
  
> Хранилище сообщений является временным и не должно быть добавлено в таблицу хранения сообщений. Когда MDB_TEMPORARY установлено, **modifyProfile** возвращает S_OK. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Изменения в разделе профилей были успешными.
    
## <a name="remarks"></a>Примечания

Для объектов поддержки поставщика сообщений реализован метод **IMAPISupport::ModifyProfile.** Поставщики магазинов сообщений **звонят в ModifyProfile,** чтобы побудить MAPI изменить сведения о профиле. 
  
 **ModifyProfile** добавляет раздел профилей, связанный с поставщиком вызовов, в список ресурсов поставщика поставщиков установленных сообщений. Это приводит к включению магазина сообщений в таблицу хранения сообщений, которая доступна клиентам с помощью метода [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) и открывается без отображения диалогового окна. 
  
Если флаг MDB_TEMPORARY, MAPI ничего не делает и метод возвращается немедленно с S_OK.
  
## <a name="see-also"></a>См. также



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

