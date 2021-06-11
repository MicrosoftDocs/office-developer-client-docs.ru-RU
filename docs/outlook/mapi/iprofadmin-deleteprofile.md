---
title: IProfAdminDeleteProfile
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.DeleteProfile
api_type:
- COM
ms.assetid: 730af2da-4c4a-42a7-9d52-56d914107d64
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8aafb849a98028efb37646752a7b49fa5e6ef2ff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419592"
---
# <a name="iprofadmindeleteprofile"></a>IProfAdmin::DeleteProfile

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет профиль.
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpszProfileName_
  
> [in] Указатель на имя удаляемого профиля.
    
 _ulFlags_
  
> [in] Всегда NULL. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Профиль был успешно удален.
    
MAPI_E_NOT_FOUND 
  
> Указанного профиля не существует.
    
## <a name="remarks"></a>Примечания

Метод **IProfAdmin::D eleteProfile** удаляет профиль. Если удалить профиль используется при призыве **DeleteProfile,** **DeleteProfile** возвращает S_OK, но не удаляет профиль немедленно. Вместо этого **DeleteProfile** отмечает профиль для удаления и удаляет его после того, как он больше не используется, когда все его активные сеансы закончились. 
  
Функция точки входа для каждой службы сообщений в профиле называется с MSG_SERVICE_DELETE в параметре _ulContext._ Сначала функция удаляет службу, а затем удаляет раздел профилей службы. Функция точки входа службы сообщений не будет снова вызвана после удаления службы. 
  
Для удаления профиля не требуется пароль.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrRemoveProfile  <br/> |MFCMAPI использует **метод IProfAdmin::D eleteProfile** для удаления выбранного профиля.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

