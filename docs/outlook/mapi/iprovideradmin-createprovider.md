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
ms.openlocfilehash: f76b44b3718f08eb68fc956ad4480d4327cb0656
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578628"
---
# <a name="iprovideradmincreateprovider"></a>IProviderAdmin::CreateProvider

**Относится к**: Outlook 2013 | Outlook 2016 
  
Добавление поставщика услуг службы сообщений. 
  
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
  
> [in] Указатель на имя поставщика для добавления.
    
 _cValues_
  
> [in] Количество значений свойств, на который указывает параметр _lpProps_ . 
    
 _lpProps_
  
> [in] Указатель на массив значений свойств, с описанием свойства поставщика для добавления.
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод. Если флаг MAPI_DIALOG установлен в параметре _ulFlags_ используется параметр _ulUIParam_ . 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который управляет добавлением поставщика. Можно задать следующие флажки:
    
  - MAPI_DIALOG: Отображает диалоговое окно для запроса сведений о конфигурации.
      
  - MAPI_UNICODE: Свойства name и строка поставщика, в формате Юникод. Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.
    
 _lpUID_
  
> [out] Указатель на структуру [MAPIUID](mapiuid.md) , содержащую уникальный идентификатор, представляющий поставщика для добавления. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Поставщик был успешно добавлена в службу сообщения.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Замечания

Метод **IProviderAdmin::CreateProvider** добавляет поставщика услуг службы сообщений. Параметр _lpszProvider_ должен указывать имя поставщика, к которой принадлежит служба сообщений. **CreateProvider** не проверяет, соответствует ли имя имя поставщика в службе; Если переданный имя не соответствует имени службы, вызов выполняется успешно, но результаты непредсказуемы. Большинство служб сообщения не разрешать поставщиков добавить или удалить профиль во время работы. 
  
Когда все доступные сведения о службе поставщика был добавлен к профилю из файла Mapisvc.inf **CreateProvider** вызывает функцию точки входа службы сообщений вместе с параметром _ulContext_ , задайте значение MSG_SERVICE_ PROVIDER_CREATE. Если в параметре метода **CreateProvider** _ulFlags_ MAPI_DIALOG, значения в параметрах _ulUIParam_ и _ulFlags_ также передаются в функцию точки входа. Эти дополнительные параметры включения поставщика услуг открыть окно свойств, поэтому пользователь может ввести параметры конфигурации. 
  
## <a name="see-also"></a>См. также

- [MAPIUID](mapiuid.md)  
- [MSGSERVICEENTRY](msgserviceentry.md)  
- [SPropValue](spropvalue.md)  
- [IProviderAdmin : IUnknown](iprovideradminiunknown.md)

