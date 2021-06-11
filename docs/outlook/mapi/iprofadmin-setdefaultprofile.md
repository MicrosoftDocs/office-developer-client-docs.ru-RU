---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 44be43864d943257520f27297e5754a4978c568d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439627"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает или очищает профиль клиента по умолчанию.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpszProfileName_
  
> [in] Указатель на имя профиля, который станет по умолчанию, или NULL. Настройка  _lpszProfileName_ в NULL указывает на то, что **SetDefaultProfile** должен удалить существующий профиль по умолчанию, оставив клиента без по умолчанию. 
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют тип строки, на которую указывает _lpszProfileName._ Можно установить следующий флаг:
    
MAPI_UNICODE 
  
> Имя профиля находится в формате Unicode. Если флаг MAPI_UNICODE не установлен, имя профиля находится в формате ANSI.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> По умолчанию был успешно создан или удален профиль по умолчанию.
    
MAPI_E_NOT_FOUND 
  
> Указанного профиля не существует.
    
## <a name="remarks"></a>Примечания

Метод **IProfAdmin::SetDefaultProfile** либо устанавливает определенный профиль в качестве профиля клиента по умолчанию, либо очищает текущий профиль по умолчанию. Профиль по умолчанию — это профиль, который автоматически используется при начале сеанса MAPI клиентом. **SetDefaultProfile** также задает свойство PR_DEFAULT_PROFILE **нового** профиля по умолчанию [(PidTagDefaultProfile).](pidtagdefaultprofile-canonical-property.md)
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы начать сеанс с профилем по умолчанию, передайте флаг MAPI_USE_DEFAULT в [функцию MAPILogonEx.](mapilogonex.md) 
  
## <a name="see-also"></a>См. также



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[Каноническое свойство PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

