---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c3c4ac10003aad8949de94e0f144410af10078b1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437240"
---
# <a name="iprofadmincopyprofile"></a>IProfAdmin::CopyProfile

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Копирует профиль.
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpszOldProfileName_
  
> [in] Указатель на имя профиля, который необходимо скопировать.
    
 _lpszOldPassword_
  
> [in] Указатель на пароль профиля, который необходимо скопировать.
    
 _lpszNewProfileName_
  
> [in] Указатель на новое имя скопированного профиля.
    
 _ulUIParam_
  
> [in] Handle to the parent window of any dialog boxes or windows that this method displays.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет копированием профиля. Можно установить следующие флаги:
    
MAPI_DIALOG 
  
> Отображает диалоговое окно, в которое пользователю будет предложено скопировать правильный пароль профиля. Если этот флаг не установлен, диалоговое окно не отображается.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Профиль успешно скопирован.
    
MAPI_E_ACCESS_DENIED 
  
> Имя нового профиля такое же, как у существующего профиля.
    
MAPI_E_LOGON_FAILED 
  
> Неправильный пароль для скопируйте профиль, и пользователю не удалось отобразить диалоговое окно для запроса правильного пароля, так как MAPI_DIALOG не задан в параметре _ulFlags._ 
    
MAPI_E_NOT_FOUND 
  
> Указанный профиль не существует.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Метод **IProfAdmin::CopyProfile** создает копию профиля, на который указывает _lpszOldProfileName,_ придавая ему имя, на которое указывает _lpszNewProfileName._ Копирование профиля оставляет копию с тем же паролем, что и исходный.
  
Имя исходного профиля, его пароль и копия могут иметь длину до 64 символов и могут включать следующие символы:
  
- Все буквы и цифры, включая знаки акцента и символ подчеркиваения.
    
- Внедренные пробелы, но не пробелы в первой или вехе.
    
Пароли профилей не поддерживаются во всех операционных системах. В операционных системах, которые не поддерживают пароли профилей,  _lpszOldPassword_ может иметь значение NULL или указатель на строку нулевой длины. 
  
Если  _для lpszOldPassword_ установлено nULL, для копируется профиль требуется пароль, а также MAPI_DIALOG флаг; Отобразилось диалоговое окно с запросом вводить пароль. Если пароль обязален, но для  _lpszOldPassword_ установлено MAPI_DIALOG NULL, **copyProfile** возвращает MAPI_E_LOGON_FAILED. 
  
## <a name="see-also"></a>См. также



[IProfAdmin : IUnknown](iprofadminiunknown.md)

