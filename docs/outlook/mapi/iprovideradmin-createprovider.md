---
title: IProviderAdminCreateProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.CreateProvider
api_type:
- COM
ms.assetid: 80c1449a-6cd9-4b93-a300-395979894b71
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 72dddca5a8079374600e05b96a24cbbc25e7f7f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430807"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**Область применения**: Outlook 2013 | Outlook 2016 
  
Добавляет поставщика услуг в службу сообщений. 
  
```cpp
HRESULT CreateProvider(
  LPSTR lpszProvider,
  ULONG cValues,
  LPSPropValue lpProps,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  MAPIUID FAR * lpUID
);
```

## <a name="parameters"></a>Parameters

 _lpszProvider_
  
> [in] Указатель на имя поставщика для добавления.
    
 _cValues_
  
> [in] Количество значений свойств, на которые указывает параметр _lpProps._ 
    
 _lpProps_
  
> [in] Указатель на массив значений свойств, описывая свойства, которые должен добавить поставщик.
    
 _ulUIParam_
  
> [in] Ручка родительского окна любых диалогов или окон, отображаемая этим методом. Параметр _ulUIParam_ используется, если флаг MAPI_DIALOG в _параметре ulFlags._ 
    
 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют добавление поставщика. Можно установить следующие флаги:
    
  - MAPI_DIALOG: отображает диалоговое окно для запроса сведений о конфигурации.
      
  - MAPI_UNICODE. Свойства имени и строки поставщика находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.
    
 _lpUID_
  
> [вышел] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор, который представляет поставщика для добавления. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Поставщик успешно добавлен в службу сообщений.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Метод **IProviderAdmin::CreateProvider** добавляет поставщика услуг в службу сообщений. Параметр  _lpszProvider должен_ указать имя поставщика, который принадлежит службе сообщений. **CreateProvider** не проверяет, соответствует ли имя поставщика в службе; если переданное имя не совпадает с именем службы, вызов удался, но результаты непредсказуемы. Большинство служб сообщений не позволяют добавлять или удалять поставщиков во время использования профиля. 
  
После того как в профиль из файла Mapisvc.inf были добавлены все доступные сведения о поставщике услуг, **CreateProvider** вызывает функцию точки входа службы сообщений с параметром  _ulContext,_ заданным MSG_SERVICE_PROVIDER_CREATE. Если MAPI_DIALOG задан в параметре _ulFlags_ метода **CreateProvider,** значения _ulUIParam_ и _ulFlags_ также передаются функции точки входа. Эти дополнительные параметры позволяют поставщику услуг отображать свой лист свойств, чтобы пользователь может ввести параметры конфигурации. 
  
## <a name="see-also"></a>См. также

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

