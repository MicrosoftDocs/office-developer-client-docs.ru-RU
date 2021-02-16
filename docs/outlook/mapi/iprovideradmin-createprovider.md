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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Добавляет поставщика службы в службу сообщений. 
  
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

## <a name="parameters"></a>Параметры

 _lpszProvider_
  
> [in] Указатель на имя добавляемого поставщика.
    
 _cValues_
  
> [in] Количество значений свойств, на которые указывает параметр _lpProps._ 
    
 _lpProps_
  
> [in] Указатель на массив значений свойств, описывая свойства добавляемого поставщика.
    
 _ulUIParam_
  
> [in] Handle to the parent window of any dialog boxes or windows this method displays. Параметр _ulUIParam_ используется, если MAPI_DIALOG флага в _параметре ulFlags._ 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет добавлением поставщика. Можно установить следующие флаги:
    
  - MAPI_DIALOG: отображает диалоговое окно с запросом сведений о конфигурации.
      
  - MAPI_UNICODE: имя поставщика и строковые свойства имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, эти строки имеют формат ANSI.
    
 _lpUID_
  
> [out] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор, который представляет добавляемого поставщика. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Поставщик успешно добавлен в службу сообщений.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Метод **IProviderAdmin::CreateProvider** добавляет поставщика службы в службу сообщений. Параметр  _lpszProvider_ должен указать имя поставщика, который принадлежит службе сообщений. **CreateProvider** не проверяет, соответствует ли имя имени поставщика в службе; Если переданное имя не совпадает с именем службы, вызов будет успешным, но результаты будут непредсказуемыми. Большинство служб сообщений не позволяют добавлять или удалять поставщиков, пока используется профиль. 
  
После того как все доступные сведения о поставщике службы были добавлены в профиль из файла Mapisvc.inf, **CreateProvider** вызывает функцию точки входа службы сообщений с параметром  _ulContext,_ для MSG_SERVICE_PROVIDER_CREATE. Если MAPI_DIALOG в параметре _ulFlags_ метода **CreateProvider,** значения _параметров ulUIParam_ и _ulFlags_ также передаются функции точки входа. Эти дополнительные параметры позволяют поставщику услуг отображать лист свойств, чтобы пользователь ввести параметры конфигурации. 
  
## <a name="see-also"></a>См. также

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

