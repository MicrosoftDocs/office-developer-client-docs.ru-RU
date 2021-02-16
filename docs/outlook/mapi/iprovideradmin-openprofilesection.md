---
title: IProviderAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: b73cf770-8817-4a23-bd14-7b76fedef214
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b3ac1b2cf8335c5e0953fdcf61b2b5d466fbb724
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405662"
---
# <a name="iprovideradminopenprofilesection"></a>IProviderAdmin::OpenProfileSection

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает раздел профиля из текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа. 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>Параметры

 _lpUID_
  
> [in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор открываемого раздела профиля. Клиенты не должны передавать NULL для _параметра lpUID._ Поставщики услуг могут передавать NULL для получения **MAPIUID** при вызове из функций точки входа службы сообщений. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса( IID), который представляет интерфейс, используемый для доступа к разделу профиля. Передача NULL приводит к возвращению стандартного интерфейса раздела профиля **(IProfSect).** 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием раздела профиля. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **openProfileSection** успешно возвращаться, возможно, до того, как раздел профиля будет полностью доступен вызываемой. Если раздел профиля не доступен, последующий вызов может вызвать ошибку. 
    
MAPI_MODIFY 
  
> Запрашивает разрешение на чтение и записи. По умолчанию объекты открываются с разрешением только для чтения, и звоня таким объектам не следует работать при предположении, что разрешение на чтение и записи предоставлено. Клиентам не разрешено разрешение на чтение и записи для разделов профиля поставщика.
    
MAPI_FORCE_ACCESS
  
> Разрешает доступ ко всем разделам профилей, даже тем, которые принадлежат отдельным поставщикам услуг.
    
 _lppProfSect_
  
> [out] Указатель на указатель на раздел профиля.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Раздел профиля успешно открыт.
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка изменить раздел профиля, доступный только для чтения, или получить доступ к объекту, у которого у пользователя недостаточно разрешений.
    
MAPI_E_NOT_FOUND 
  
> Запрашиваемая часть профиля не существует.
    
## <a name="remarks"></a>Примечания

Метод **IProviderAdmin::OpenProfileSection** открывает раздел профиля, позволяя звоняшему считывать сведения из активного профиля и, возможно, записывать данные в него. 
  
Клиенты не могут открывать разделы профилей, принадлежащие поставщикам, с помощью метода **OpenProfileSection.** 
  
Несколько клиентов или поставщиков услуг могут одновременно открывать раздел профиля с разрешением только для чтения. Однако, когда раздел профиля открыт с разрешением на чтение и записи, никакие другие вызовы не могут быть сделаны для открытия раздела, независимо от типа доступа. Если раздел профиля открыт с разрешением только для чтения, последующий вызов запроса разрешения на чтение и записи не будет MAPI_E_NO_ACCESS. Аналогично, если раздел открыт с разрешением на чтение и записи, последующий вызов запроса разрешения только для чтения также не удастся. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если вы запросили **openProfileSection** открыть несуществов раздел профиля, передав MAPI_MODIFY в  _ulFlags_ и неизвестный **MAPIUID** в  _lpUID,_ будет создан раздел профиля. 
  
Если вы запросили, чтобы **OpenProfileSection** открывал несущестуальный раздел с разрешением только для чтения, оно возвращает MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI использует метод **IProviderAdmin::OpenProfileSection** для открытия раздела профиля из текущего профиля.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

