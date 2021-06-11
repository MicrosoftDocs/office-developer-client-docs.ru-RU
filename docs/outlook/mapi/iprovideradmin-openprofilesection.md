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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает раздел профилей из текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа. 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>Parameters

 _lpUID_
  
> [in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор для открываемого раздела профиля. Клиенты не должны передавать NULL для _параметра lpUID._ Поставщики служб могут передать NULL для получения **MAPIUID** при вызове из функций точки входа в службу сообщений. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к разделу профилей. Передача NULL приводит к возвращению стандартного интерфейса раздела профилей **(IProfSect).** 
    
 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют открытие раздела профилей. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenProfileSection** успешно возвращаться, возможно, до того, как раздел профилей будет полностью доступен вызываемой. Если раздел профилей не доступен, последующий вызов может привести к ошибке. 
    
MAPI_MODIFY 
  
> Запросы на чтение и написание разрешений. По умолчанию объекты открываются только для чтения, и звонителям не следует работать с предположением о том, что разрешение на чтение и записи было предоставлено. Клиентам не разрешается читать и писать разрешения для поставщиков разделов профиля.
    
MAPI_FORCE_ACCESS
  
> Позволяет получить доступ ко всем разделам профилей, даже к разделам, которые принадлежат отдельным поставщикам услуг.
    
 _lppProfSect_
  
> [вышел] Указатель на указатель в разделе профиль.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Раздел профилей был успешно открыт.
    
MAPI_E_NO_ACCESS 
  
> Была предпринята попытка изменить раздел профиля только для чтения или получить доступ к объекту, для которого у пользователя недостаточно разрешений.
    
MAPI_E_NOT_FOUND 
  
> Запрашиваемая часть профиля не существует.
    
## <a name="remarks"></a>Примечания

Метод **IProviderAdmin::OpenProfileSection** открывает профильный раздел, позволяющий звоняшему считывать сведения из активного профиля и, возможно, записывать сведения. 
  
Клиенты не могут открывать разделы профилей, принадлежащие поставщикам, с помощью метода **OpenProfileSection.** 
  
Несколько клиентов или поставщиков услуг могут одновременно открывать раздел профилей с разрешения только для чтения. Однако, когда раздел профиля открыт с разрешением на чтение и записи, никакие другие вызовы не могут быть сделаны, чтобы открыть раздел, независимо от типа доступа. Если раздел профилей открыт с разрешения только для чтения, последующий вызов запроса разрешения на чтение и написание не удастся MAPI_E_NO_ACCESS. Кроме того, если раздел открыт с разрешением на чтение и написание, последующий вызов запроса разрешения только для чтения также не удастся. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если вы хотите, чтобы **OpenProfileSection** открыл несуществовный раздел профиля, передав MAPI_MODIFY в  _ulFlags_ и неизвестный **MAPIUID** в  _lpUID,_ будет создан раздел профилей. 
  
Если вы хотите, **чтобы OpenProfileSection** открыл несуществовной раздел с разрешения только для чтения, он возвращает MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI использует **метод IProviderAdmin::OpenProfileSection** для открытия раздела профиля из текущего профиля.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

