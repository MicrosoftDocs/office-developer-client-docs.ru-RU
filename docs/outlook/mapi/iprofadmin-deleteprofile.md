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
ms.openlocfilehash: 249d2dcf3a298abde85bdc53620680146d43c168
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809521"
---
# <a name="iprofadmindeleteprofile"></a>IProfAdmin::DeleteProfile

  
  
**Относится к**: Outlook 
  
Удаляет профиль.
  
```cpp
HRESULT DeleteProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpszProfileName_
  
> [in] Указатель на имя профиля, который требуется удалить.
    
 _ulFlags_
  
> [in] Всегда имеет значение NULL. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Профиль успешно удален.
    
MAPI_E_NOT_FOUND 
  
> Указанный профиль не существует.
    
## <a name="remarks"></a>Замечания

Метод **IProfAdmin::DeleteProfile** удаляет профиль. Если профиль для удаления используется при вызове **DeleteProfile** , **DeleteProfile** возвращает значение S_OK, но не удаляет профиль немедленно. Вместо этого **DeleteProfile** помечает профиля для удаления и удаляется после его больше не используется, по окончании всех активных сеансов. 
  
С MSG_SERVICE_DELETE значение, установленное в параметре _ulContext_ вызывает функцию точки входа для каждой службы сообщений в профиле. Во-первых функция удаляет службу, а затем его удаляет раздел службы профилей. После удаления службы функцию точки входа службы сообщений не вызывает еще раз. 
  
Чтобы удалить профиль необходим не пароль.
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrRemoveProfile  <br/> |Mfcmapi (en) метод **IProfAdmin::DeleteProfile** используется для удаления выбранного профиля.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
