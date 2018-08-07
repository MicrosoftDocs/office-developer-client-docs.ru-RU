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
ms.openlocfilehash: 3cd1a19b23a3c4d3ff8a297881eb2b959585eb17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809873"
---
# <a name="mapiadminprofiles"></a>MAPIAdminProfiles

  
  
**Относится к**: Outlook 
  
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

