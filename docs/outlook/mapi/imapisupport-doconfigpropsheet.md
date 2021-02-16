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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отображает таблицу свойств конфигурации.
  
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

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window of the property sheet.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpszTitle_
  
> [in] Указатель на заголовок листа свойств.
    
 _lpDisplayTable_
  
> [in] Указатель на таблицу отображения, описывая элементы управления, отображаемую на листе свойств.
    
 _lpConfigData_
  
> [in] Указатель на реализацию [IMAPIProp,](imapipropiunknown.md) которая будет использоваться для доступа к свойствам конфигурации, отображаемой на листе свойств. 
    
 _ulTopPage_
  
> [in] Индекс с нулем на верхней странице таблицы свойств по умолчанию.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Отобразилась таблица свойств конфигурации.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::D oConfigPropsheet** реализован для всех объектов поддержки. **DoConfigPropSheet** предоставляет стандартный пользовательский интерфейс для отображения свойств поставщиков услуг и служб сообщений. Это стандартное диалоговое окно следует использовать для всех отображаемого свойства конфигурации, чтобы пользователи могли использовать согласованный интерфейс Windows. 
  
Поставщики услуг вызывают **DoConfigPropSheet** в рамках реализации метода [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) или с кнопки, используемой для отображения сведений о свойствах. Службы сообщений **звонят в DoConfigPropSheet из** функции точки входа службы сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Таблицу отображения, на которая указывает  _параметр lpDisplayTable,_ можно создать, вызывая функцию [BuildDisplayTable](builddisplaytable.md) или с помощью пользовательского кода. 
  
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

