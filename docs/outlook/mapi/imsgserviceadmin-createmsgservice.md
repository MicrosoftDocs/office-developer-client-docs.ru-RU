---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e7d30c1aba8ddc1419045c1caa8524f7d2063dc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434979"
---
# <a name="imsgserviceadmincreatemsgservice"></a>IMsgServiceAdmin::CreateMsgService

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Рекомендуется использовать [IMsgServiceAdmin2::CreateMsgServiceEx.](imsgserviceadmin2-createmsgserviceex.md) Добавляет службу сообщений в текущий профиль. 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
);
```

## <a name="parameters"></a>Parameters

 _lpszService_
  
> [in] Указатель на имя службы сообщений для добавления. Это имя службы сообщений должно отображаться в **разделе [Services]** файла MapiSvc.inf. 
    
 _lpszDisplayName_
  
> [in] Указатель на отображаемого имени службы сообщений для добавления. Параметр  _lpszDisplayName_ **игнорируется,** если служба сообщений задает свойство [PR_DISPLAY_NAME (PidTagDisplayName)](pidtagdisplayname-canonical-property.md)в файле MapiSvc.inf.
    
 _ulUIParam_
  
> [in] Ручка родительского окна любых диалогов или окон, отображаемая этим методом.
    
 _ulFlags_
  
> [in] Немного флагов, которые контролируют установку службы сообщений. Можно установить следующие флаги:
    
MAPI_UNICODE
  
> Параметры lpszService и lpszDisplayName должны быть отлиты в LPWSTR и интерпретированы как строки Юникод.
    
SERVICE_NO_RESTART_WARNING
  
> При добавлении новой службы сообщений в профиль подсистема MAPI, основанная на различных обстоятельствах и критериях, часто определяет, что это действие требует перезапуска Outlook. Если флаг SERVICE_NO_RESTART_WARNING не включен, а пользовательский интерфейс разрешен на основе флагов SERVICE_UI_ALWAYS и SERVICE_UI_ALLOWED, и по крайней мере один процесс вошел в текущий профиль, эта функция отображает сообщение "Необходимо перезапустить Outlook, чтобы эти изменения вступили в силу". В том числе SERVICE_NO_RESTART_WARNING подавляет отображение этого предупреждаемого сообщения.
    
SERVICE_UI_ALLOWED
  
> Пользовательский интерфейс конфигурации службы сообщений допускается при необходимости.
    
SERVICE_UI_ALWAYS 
  
> Служба сообщений отображает свой лист свойств конфигурации.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NOT_FOUND 
  
> Имя службы сообщений не находится в **разделе [Services]** MapiSvc.inf. 
    
## <a name="remarks"></a>Примечания

Метод **IMsgServiceAdmin::CreateMsgService** добавляет службу сообщений в текущий профиль. **CreateMsgService** вызывает функцию точки входа службы сообщений для выполнения любых задач конфигурации, определенных для службы. Если флаг SERVICE_UI_ALLOWED установлен в параметре  _ulFlags,_ установленная служба сообщений может отображать лист свойств, позволяющий пользователю настраивать его параметры. 
  
Файл MapiSvc.inf содержит список поставщиков, которые составляют службу сообщений, и свойства для каждого из них. **CreateMsgService** сначала создает новый раздел профиля для службы сообщений, а затем копирует всю информацию для этой службы из файла MapiSvc.inf в профиль, создавая новые разделы для каждого поставщика. 
  
После скопив всю информацию из MapiSvc.inf, функция точки входа службы сообщений называется с MSG_SERVICE_CREATE значением в параметре _ulContext._ Если флаг SERVICE_UI_ALLOWED задан в параметре _ulFlags_ метода **CreateMsgService,** значения _ulUIParam_ и _ulFlags_ также передаются, когда называется функция точки входа службы сообщений. Поставщики служб должны отображать свои таблицы свойств конфигурации, чтобы пользователи могли настроить службу сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **CreateMsgService** не возвращает структуру [MAPIUID](mapiuid.md) для службы сообщений, добавленной в профиль. 
  
Чтобы получить **MAPIUID для** созданной службы сообщений, используйте следующую процедуру: 
  
1. Чтобы получить таблицу администрирования сообщений, позвоните в [метод IMsgServiceAdmin::GetMsgServiceTable.](imsgserviceadmin-getmsgservicetable.md) 
    
2. Найдите строку, которая представляет службу сообщений, разместив ограничение на таблице, которая соответствует свойству **PR_SERVICE_NAME** [(PidTagServiceName)](pidtagservicename-canonical-property.md)с именем службы сообщений. 
    
3. Извлечение свойства **PR_SERVICE_UID** [(PidTagServiceUid).](pidtagserviceuid-canonical-property.md) 
    
4. Передай значение свойства **PR_SERVICE_UID**  _параметра lpUid_ [методу IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) для настройки службы. 
    
> [!CAUTION]
> Реализация Microsoft Outlook 2010, русская версия MAPI не поддерживает MAPI_UNICODE, если она используется. 
  
> [!IMPORTANT]
> Значение  _ulFlags_ SERVICE_NO_RESTART_WARNING не может быть определено в загружаемом файле заголовки, который в настоящее время имеется, и в этом случае его можно добавить в код, используя следующее значение: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI использует **метод IMsgServiceAdmin::CreateMsgService** для добавления службы в профиль.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

