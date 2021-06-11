---
title: IMAPISupportDoConfigPropsheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoConfigPropsheet
api_type:
- COM
ms.assetid: 3899c49c-a0ec-4dca-92e8-e801cd4908cf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cd8727104af694d456074614b5ea7c222c9b91b9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429019"
---
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отображает лист свойств конфигурации.
  
```cpp
HRESULT DoConfigPropsheet(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszTitle,
  LPMAPITABLE lpDisplayTable,
  LPMAPIPROP lpConfigData,
  ULONG ulTopPage
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна листа свойств.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpszTitle_
  
> [in] Указатель на название листа свойств.
    
 _lpDisplayTable_
  
> [in] Указатель на таблицу отображения, описывая элементы управления, которые отображаются на листе свойств.
    
 _lpConfigData_
  
> [in] Указатель на реализацию [IMAPIProp,](imapipropiunknown.md) которая будет использоваться для доступа к свойствам конфигурации, отображаемым на листе свойств. 
    
 _ulTopPage_
  
> [in] Нулевой индекс на верхней странице свойства по умолчанию.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Отображается лист свойств конфигурации.
    
## <a name="remarks"></a>Примечания

Для всех объектов поддержки **реализован метод IMAPISupport::D oConfigPropsheet.** **DoConfigPropSheet** предоставляет стандартный пользовательский интерфейс для отображения свойств поставщиков услуг и служб сообщений. Этот стандартный диалоговое окно следует использовать для всех отображаемого свойства конфигурации, чтобы пользователи могли использовать Windows интерфейса. 
  
Поставщики услуг звонят **в DoConfigPropSheet** в рамках реализации метода [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) или с кнопки, используемой для отображения сведений о свойствах. Службы сообщений звонят **в DoConfigPropSheet** из своей функции точки входа в службу сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Таблицу отображения можно создать с помощью  _параметра lpDisplayTable,_ назвав функцию [BuildDisplayTable](builddisplaytable.md) или с помощью пользовательского кода. 
  
## <a name="see-also"></a>См. также



[BuildDisplayTable](builddisplaytable.md)
  
[CreateIProp](createiprop.md)
  
[IABProvider::Logon](iabprovider-logon.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

