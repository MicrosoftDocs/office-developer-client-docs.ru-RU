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
ms.openlocfilehash: 87ac394f9ab77b092cdfcd44f65b040a039319e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422189"
---
# <a name="imsgserviceadminconfiguremsgservice"></a>IMsgServiceAdmin::ConfigureMsgService

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Перенастройка службы сообщений.
  
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
  
> [in] Указатель на структуру [MAPIUID,](mapiuid.md) которая содержит уникальный идентификатор для службы сообщений, которую необходимо настроить. 
    
 _ulUIParam_
  
> [in] Окне родительского окна таблицы свойств конфигурации.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет отображением листа свойств. Можно установить следующие флаги:
    
MAPI_UNICODE 
  
> Переданные строки имеют формат Юникод. Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.
    
MSG_SERVICE_UI_READ_ONLY 
  
> Служба сообщений должна отобразить свою таблицу свойств конфигурации, но не позволить пользователю изменить ее. Большинство служб сообщений игнорируют этот флаг.
    
SERVICE_UI_ALLOWED 
  
> Таблица свойств конфигурации службы сообщений должна отображаться только в том случае, если служба не настроена полностью.
    
SERVICE_UI_ALWAYS 
  
> Служба сообщений всегда должна отображать свою таблицу свойств конфигурации. Если SERVICE_UI_ALWAYS не задан, лист свойств конфигурации по-прежнему может отображаться, если SERVICE_UI_ALLOWED задан и допустимые сведения о конфигурации недоступны из массива значений свойств в параметре _lpProps._ Для SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS необходимо настроить таблицу свойств. 
    
 _cValues_
  
> [in] Количество значений свойств в [структуре SPropValue,](spropvalue.md) на которые указывает _lpProps._ 
    
 _lpProps_
  
> [in] Указатель на массив значений свойств, которые описывают свойства, отображаемую на листе свойств. Параметр  _lpProps_ не должен иметь NULL, если служба сообщений должна быть настроена без пользовательского интерфейса. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Служба сообщений успешно настроена.
    
MAPI_E_EXTENDED_ERROR 
  
> Ошибка, относяная к службе сообщений. Чтобы получить [структуру MAPIERROR,](mapierror.md) описываемую ошибку, клиентский приложение должно вызвать метод [IMsgServiceAdmin::GetLastError.](imsgserviceadmin-getlasterror.md) 
    
MAPI_E_NOT_FOUND 
  
> **MAPIUID, на** который указывает _lpUID,_ не совпадает с интерфейсом MAPIUID существующей службы сообщений. 
    
MAPI_E_NOT_INITIALIZED 
  
> Служба сообщений не имеет функции точки входа.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, обычно нажав  кнопку "Отмена" на листе свойств. 
    
## <a name="remarks"></a>Примечания

Метод **IMsgServiceAdmin::ConfigureMsgService** позволяет настроить службу сообщений с листом свойств конфигурации или без нее. 
  
Чтобы разрешить настройку без отображения листа свойств, службы сообщений обычно подготавливают файл загона, который содержит константы для всех необходимых и необязательных свойств и их значений.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы получить структуру **MAPIUID** для службы сообщений, необходимо получить столбец **PR_SERVICE_UID** [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md)из строки службы сообщений в таблице службы сообщений. Дополнительные сведения см. в процедуре, описанной в методе [IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md) 
  
Вы можете настроить службу сообщений, не отображая лист свойств для пользователя, только если у вас есть дополнительные сведения о значениях свойств, которые необходимо установить. Если служба сообщений настраивается без отображения листа свойств, передав допустимые значения свойств в  _параметре lpProps_ и не устанавливая флаги MSG_SERVICE_UI_READ_ONLY, SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS. 
  
Если вы получаете все или некоторые сведения о конфигурации от пользователя с помощью листа свойств, установите SERVICE_UI_ALLOWED _в ulFlags._ Если сведения о существующем свойстве используются только для установки параметров по умолчанию и пользователь может изменить эти параметры, установите SERVICE_UI_ALWAYS в _ulFlags._
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI использует метод **IMsgServiceAdmin::ConfigureMsgService** для настройки службы, добавленной в профиль.  <br/> |
   
## <a name="see-also"></a>См. также



[MAPIUID](mapiuid.md)
  
[SPropValue](spropvalue.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

