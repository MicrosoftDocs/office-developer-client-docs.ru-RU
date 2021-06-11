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
ms.openlocfilehash: e5043a614ccd94994fe86838f15aa1a43f22733e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412354"
---
# <a name="mapiadminprofiles"></a>MAPIAdminProfiles

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает объект администрирования профилей. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] Bitmask флагов с указанием параметров для функции входа в службу. 
    
 _lppProfAdmin_
  
> [вышел] Указатель на указатель на новый объект администрирования профиля.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::GetProfAdmin  <br/> |MFCMAPI использует **метод MAPIAdminProfiles** для получения объекта администрирования профиля.  <br/> |
   
## <a name="see-also"></a>См. также



[IProfAdmin::CreateProfile](iprofadmin-createprofile.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

