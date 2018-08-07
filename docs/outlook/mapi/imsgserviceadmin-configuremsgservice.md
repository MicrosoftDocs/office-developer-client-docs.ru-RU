---
title: IMsgServiceAdminConfigureMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.ConfigureMsgService
api_type:
- COM
ms.assetid: a08f5905-2585-49ca-abb7-a77f2736f604
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f58d0f5cd7dfe74d3859d4f06a41aad6c3a55ac4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809336"
---
# <a name="imsgserviceadminconfiguremsgservice"></a>IMsgServiceAdmin::ConfigureMsgService

  
  
**Относится к**: Outlook 
  
Устанавливает службы сообщений.
  
```cpp
HRESULT ConfigureMsgService(
  LPMAPIUID lpUID,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpProps
);
```

## <a name="parameters"></a>Параметры

 _lpUID_
  
> [in] Указатель на структуру [MAPIUID](mapiuid.md) , который содержит уникальный идентификатор для службы сообщений для настройки. 
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна окно свойств конфигурации.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее отображение страницы свойств. Можно задать следующие флажки:
    
MAPI_UNICODE 
  
> Строки переданное хранятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, они в формате ANSI.
    
MSG_SERVICE_UI_READ_ONLY 
  
> Служба сообщений следует открыть окно свойств конфигурации, но не включать изменения пользователем. Большинство служб сообщение пропустить этот флаг.
    
SERVICE_UI_ALLOWED 
  
> Служба сообщений следует открыть окно свойств конфигурации только в том случае, если служба не завершена.
    
SERVICE_UI_ALWAYS 
  
> Служба сообщений всегда должен открыть окно свойств конфигурации. Если SERVICE_UI_ALWAYS не задано, свойств конфигурации может по-прежнему отображается, если установлено SERVICE_UI_ALLOWED и сведений о конфигурации допустимый недоступен из массива значение свойства с помощью параметра _lpProps_ . SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS должно иметь значение для свойств для отображения. 
    
 _cValues_
  
> [in] Число значений свойств в структуре [SPropValue](spropvalue.md) , на который указывает _lpProps_. 
    
 _lpProps_
  
> [in] Указатель на массив значений свойств, которые описывают свойства для отображения в окне свойств. Параметр _lpProps_ не должен быть NULL, если служба сообщений, необходимо настроить без пользовательского интерфейса. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Служба сообщений успешно настроено.
    
MAPI_E_EXTENDED_ERROR 
  
> Ошибка специально для службы сообщений. Чтобы получить структура [MAPIERROR](mapierror.md) с описанием ошибки, клиентское приложение следует вызовите метод [IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md) . 
    
MAPI_E_NOT_FOUND 
  
> **MAPIUID** , на который указывает _lpUID_ не совпадает с существующей службы сообщений. 
    
MAPI_E_NOT_INITIALIZED 
  
> Служба сообщений не имеет функцию точки входа.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** на странице свойств. 
    
## <a name="remarks"></a>Замечания

Метод **IMsgServiceAdmin::ConfigureMsgService** позволяет службы сообщений, который требуется настроить, независимо от настройки свойств. 
  
Чтобы разрешить конфигурации без отображение листа свойств, службы сообщений обычно Подготовьте файл заголовка, который включает в себя константы для все необходимые и дополнительные свойства и их значения.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Для получения **MAPIUID** структуру для настройки службы сообщений, извлечь столбец **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) из службы сообщений строку в таблице службы сообщений. Для получения дополнительных сведений см процедуры, описанные в методе [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
Для настройки службы сообщение без отображения свойств пользователю только в том случае, если у вас есть Дополнительные сведения о значения свойств должно быть задано. При настройке службы сообщений без отображения свойств, передайте допустимыми значениями свойства с помощью параметра _lpProps_ и не задано флаги MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS. 
  
Если вы получаете все или некоторые сведения о конфигурации от пользователя через страницу свойств необходимо задайте SERVICE_UI_ALLOWED в _ulFlags_. Если использовать существующие сведения о свойствах только для установки параметров по умолчанию, и пользователь может изменять параметры, задайте SERVICE_UI_ALWAYS в _ulFlags_.
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |Mfcmapi (en) использует метод **IMsgServiceAdmin::ConfigureMsgService** для настройки службы, который был добавлен в профиль.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

