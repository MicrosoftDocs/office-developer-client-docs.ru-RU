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
ms.openlocfilehash: b16730681b5414f28ae45be7195b4fa551bf0e82
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591991"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Вносятся изменения в сообщение хранения основного раздела профиля.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Хранить битовую маску флагов, указывающую тип сообщений. Можно задать следующий флаг:
    
MDB_TEMPORARY 
  
> Хранилище сообщений временно и не следует добавлять к таблице хранилища сообщений. Если для MDB_TEMPORARY, **ModifyProfile** возвращает значение S_OK немедленно. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Изменения в раздел профиля было выполнено успешно.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::ModifyProfile** реализуется для объектов поддержки поставщика хранилища сообщений. Сообщение вызова поставщиков хранилища **ModifyProfile** запроса MAPI для изменения сведения о своих профилях. 
  
 **ModifyProfile** Добавление раздела профиля, который связан с вызова поставщика в список установленных сообщение ресурсов поставщика хранилища. В этом случае хранилища сообщений и будет включено в таблицу хранилища сообщений, в которой доступен для клиентов, метод [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) и открывать без отображения диалогового окна. 
  
Если установлен флаг MDB_TEMPORARY, MAPI не выполняет никаких действий и метод немедленно возвращает значение S_OK.
  
## <a name="see-also"></a>См. также



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

