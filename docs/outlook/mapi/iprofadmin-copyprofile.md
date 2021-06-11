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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _lpszOldProfileName_
  
> [in] Указатель на имя профиля для копирования.
    
 _lpszOldPassword_
  
> [in] Указатель на пароль профиля для копирования.
    
 _lpszNewProfileName_
  
> [in] Указатель на новое имя скопированного профиля.
    
 _ulUIParam_
  
> [in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом.
    
 _ulFlags_
  
> [in] Битмашка флагов, которые контролируют копирование профиля. Можно установить следующие флаги:
    
MAPI_DIALOG 
  
> Отображает диалоговое окно, которое подсказывет пользователю правильный пароль профиля для копирования. Если этот флаг не установлен, диалоговое окно не отображается.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Профиль был успешно скопирован.
    
MAPI_E_ACCESS_DENIED 
  
> Новое имя профиля является таким же, как и существующего профиля.
    
MAPI_E_LOGON_FAILED 
  
> Пароль для копирования профиля неверен, и диалоговое окно не может отображаться пользователю для запроса правильного пароля, так как MAPI_DIALOG не был задан в параметре _ulFlags._ 
    
MAPI_E_NOT_FOUND 
  
> Указанного профиля не существует.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Метод **IProfAdmin::CopyProfile** создает копию профиля, на который указывает _lpszOldProfileName,_ придавая ему имя, на которое указывает _lpszNewProfileName._ Копирование профиля оставляет копию с тем же паролем, что и оригинал.
  
Имя исходного профиля, его пароль и копия могут иметь длину до 64 символов и включать следующие символы:
  
- Все буквы, включая символы акцента и символы подчеркнуть.
    
- Встроенные пробелы, но не ведущие и не ведущие.
    
Пароли профилей поддерживаются не во всех операционных системах. В операционных системах, которые не поддерживают пароли профилей,  _lpszOldPassword_ может быть NULL или указателем на строку нулевой длины. 
  
Если  _lpszOldPassword_ задает NULL, для скопивного профиля требуется пароль, а MAPI_DIALOG задает флаг; отображается диалоговое окно, в которое пользователь должен предоставить пароль. Если требуется пароль, но  _для lpszOldPassword_ задавалось NULL и флаг MAPI_DIALOG не установлен, **CopyProfile** возвращает MAPI_E_LOGON_FAILED. 
  
## <a name="see-also"></a>См. также



[IProfAdmin : IUnknown](iprofadminiunknown.md)

