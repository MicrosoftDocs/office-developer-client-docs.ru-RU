---
title: ипрофадминсетдефаултпрофиле
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает или очищает профиль клиента, используемый по умолчанию.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _лпсзпрофиленаме_
  
> возврата Указатель на имя профиля, который будет служить значением по умолчанию, или значение NULL. Если для параметра _лпсзпрофиленаме_ ЗАДАНО значение null, то **SetDefaultProfile** должен удалить существующий профиль по умолчанию, оставив клиент без значения по умолчанию. 
    
 _ulFlags_
  
> возврата Битовая маска флагов, определяющая тип строки, на которую указывает _лпсзпрофиленаме_. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Имя профиля имеет формат Юникод. Если флаг MAPI_UNICODE не установлен, имя профиля будет иметь формат ANSI.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Профиль по умолчанию успешно установлен или удален.
    
MAPI_E_NOT_FOUND 
  
> Указанный профиль не существует.
    
## <a name="remarks"></a>Примечания

Метод **ипрофадмин:: SetDefaultProfile** устанавливает определенный профиль в качестве профиля клиента по умолчанию или очищает текущий профиль по умолчанию. Профиль по умолчанию — это профиль, который автоматически используется всякий раз, когда клиент начинает сеанс MAPI. **SetDefaultProfile** также задает значение true для нового свойства **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) профиля по умолчанию.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы запустить сеанс с профилем по умолчанию, передайте флаг MAPI_USE_DEFAULT в функцию [мапилогонекс](mapilogonex.md) . 
  
## <a name="see-also"></a>См. также



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[Каноническое свойство PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

