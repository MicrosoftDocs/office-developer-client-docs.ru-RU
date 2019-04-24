---
title: Имаписуппортдоконфигпропшит
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322374"
---
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Отображает страницу свойств конфигурации.
  
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

 _Улуипарам_
  
> возврата Дескриптор родительского окна страницы свойств.
    
 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
 _Лпсзтитле_
  
> возврата Указатель на название страницы свойств.
    
 _Лпдисплайтабле_
  
> возврата Указатель на таблицу отображения, описывающую элементы управления, которые отображаются на странице свойств.
    
 _Лпконфигдата_
  
> возврата Указатель на реализацию [IMAPIProp](imapipropiunknown.md) , который будет использоваться для доступа к свойствам конфигурации, которые будут отображаться на странице свойств. 
    
 _Ултоппаже_
  
> возврата Индекс с отсчетом от нуля до верхней страницы листа свойств по умолчанию.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Отображается страница свойств конфигурации.
    
## <a name="remarks"></a>Замечания

Метод **имаписуппорт::D оконфигпропшит** реализован для всех объектов поддержки. **Доконфигпропшит** предоставляет стандартный пользовательский интерфейс для отображения свойств поставщиков услуг и служб сообщений. Это стандартное диалоговое окно следует использовать для всех свойств конфигурации, чтобы пользователи могли воспользоваться единообразным интерфейсом Windows. 
  
Поставщики услуг вызывают **доконфигпропшит** в рамках реализации метода [Имапистатус:: сеттингсдиалог](imapistatus-settingsdialog.md) или из кнопки, используемой для отображения сведений о свойствах. Службы сообщений вызывают **доконфигпропшит** из функции точки входа службы сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы можете создать отображаемую таблицу, на которую указывает параметр _лпдисплайтабле_ , вызвав функцию [буилддисплайтабле](builddisplaytable.md) или пользовательский код. 
  
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

