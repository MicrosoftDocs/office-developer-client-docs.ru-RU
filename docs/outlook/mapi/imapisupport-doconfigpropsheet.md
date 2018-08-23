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
ms.openlocfilehash: 3b3499de9446c83cfc3b97b4d6b02e7c430b65f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586398"
---
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Отображает окно свойств конфигурации.
  
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
  
> [in] Дескриптор родительского окна окно свойств.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _lpszTitle_
  
> [in] Указатель на заголовок страницы свойств.
    
 _lpDisplayTable_
  
> [in] Указатель на таблицу отображения, описываются элементы управления для отображения в окне свойств.
    
 _lpConfigData_
  
> [in] Указатель на реализацию [IMAPIProp](imapipropiunknown.md) для использования для доступа к свойствам конфигурации для отображения в окне свойств. 
    
 _ulTopPage_
  
> [in] Отсчитываемый от нуля индекс для в верхней части страницы по умолчанию страницу свойств.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Окно свойств конфигурации отображенные.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::DoConfigPropsheet** применяется для всех объектов поддержки. **DoConfigPropSheet** предоставляет стандартный пользовательский интерфейс для отображения свойств поставщиков услуг и службы сообщений. В этом поле стандартное диалоговое окно следует использовать для всех отображает свойства конфигурации, чтобы пользователи выгоднее согласованного интерфейса Windows. 
  
Поставщики услуг вызова **DoConfigPropSheet** как часть их реализации метода [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) или с помощью кнопки используется для отображения сведений о свойствах. Службы сообщений вызов **DoConfigPropSheet** из их функции точки входа службы сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно создать в таблице отображения, на который указывает параметр _lpDisplayTable_ путем вызова функции [BuildDisplayTable](builddisplaytable.md) или с помощью пользовательского кода. 
  
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

