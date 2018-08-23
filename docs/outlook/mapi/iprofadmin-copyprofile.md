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
ms.openlocfilehash: 9e22111ec920d89e0874baf71946681c204cacd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571208"
---
# <a name="iprofadmincopyprofile"></a>IProfAdmin::CopyProfile

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Указатель на имя профиля для копирования.
    
 _lpszOldPassword_
  
> [in] Указатель на пароль профиля для копирования.
    
 _lpszNewProfileName_
  
> [in] Указатель на новое имя скопированного профиля.
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна все диалоговые окна или окна, которые отображаются этот метод.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как скопировать конфигурацию. Можно задать следующие флажки:
    
MAPI_DIALOG 
  
> Отображает диалоговое окно, которое запрашивает у правильный пароль профиля пользователя для копирования. Если этот флаг не установлен, диалоговое окно не отображается.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Профиль успешно скопирован.
    
MAPI_E_ACCESS_DENIED 
  
> Имя нового профиля — это то же самое, что и существующий профиль.
    
MAPI_E_LOGON_FAILED 
  
> Неправильный пароль для профиля для копирования и диалоговое окно "" не удается отобразить для пользователя, чтобы запросить правильный пароль, так как MAPI_DIALOG не установлен в параметре _ulFlags_ . 
    
MAPI_E_NOT_FOUND 
  
> Указанный профиль не существует.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Замечания

Предоставляет метод **IProfAdmin::CopyProfile** , копию профиля, который указывает _lpszOldProfileName_, указав имя указывает _lpszNewProfileName_. Копирование профиля оставляет эту копию с тот же пароль, что и исходный.
  
Имя исходного профиля, его пароль и эту копию может быть длиной до 64 символов и может содержать следующие символы:
  
- Все буквенно-цифровых символов, в том числе диакритических знаков и символ подчеркивания.
    
- Пробелы, но не начальных и конечных пробелов.
    
Профиль пароли не поддерживаются для всех операционных систем. В операционных системах, которые не поддерживают пароли профилей _lpszOldPassword_ может быть NULL или указатель на строку нулевой длины. 
  
Если _lpszOldPassword_ имеет значение NULL, профиля для копирования требуется пароль, а флаг MAPI_DIALOG — значение; отображается диалоговое окно, в котором пользователь для ввода пароля. Если пароль является обязательным, но _lpszOldPassword_ имеет значение NULL и MAPI_DIALOG флаг не установлен, **CopyProfile** возвращает MAPI_E_LOGON_FAILED. 
  
## <a name="see-also"></a>См. также



[IProfAdmin : IUnknown](iprofadminiunknown.md)

