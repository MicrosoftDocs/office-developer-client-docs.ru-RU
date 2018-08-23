---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 843eed06f30dcca530cf4306c9e03bbffbb05af5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581288"
---
# <a name="mapiadminprofiles"></a>MAPIAdminProfiles

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создает объект администрирования профилей. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска, указывающее параметры для функции входа службы флагов. 
    
 _lppProfAdmin_
  
> [out] Указатель на указатель на новый объект администрирования профилей.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetProfAdmin  <br/> |Mfcmapi (en) использует метод **MAPIAdminProfiles** для получения объекта администрирования профилей.  <br/> |
   
## <a name="see-also"></a>См. также



[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

