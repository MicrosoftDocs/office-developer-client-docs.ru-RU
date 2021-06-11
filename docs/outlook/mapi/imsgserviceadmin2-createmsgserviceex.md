---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b7fe25491228f00f6865af963db36f27bae5d7a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410184"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Добавляет службу сообщений в текущий профиль и возвращает недавно добавленный UID службы.
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
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
    
 _lpuidService_
  
> [вышел] Указатель на UID добавленной службы сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NOT_FOUND
  
> Имя службы сообщений не находится в **разделе [Services]** MapiSvc.inf. 
    
## <a name="remarks"></a>Примечания

Метод **IMsgServiceAdmin2::CreateMsgServiceEx** добавляет службу сообщений в текущий профиль. **CreateMsgServiceEx** вызывает функцию точки входа службы сообщений для выполнения любых задач конфигурации, определенных для службы. Если флаг SERVICE_UI_ALLOWED установлен в параметре  _ulFlags,_ установленная служба сообщений может отображать лист свойств, позволяющий пользователю настраивать его параметры. 
  
Файл MapiSvc.inf содержит список поставщиков, которые составляют службу сообщений, и свойства для каждого из них. **CreateMsgServiceEx** сначала создает новый раздел профиля для службы сообщений, а затем копирует всю информацию для этой службы из файла MapiSvc.inf в профиль, создавая новые разделы для каждого поставщика. 
  
После копирования всех сведений из MapiSvc.inf функция точки входа службы сообщений **MSGSERVICEENTRY** вызвана с MSG_SERVICE_CREATE значением в параметре _ulContext._ Если флаг SERVICE_UI_ALLOWED установлен в параметре _ulFlags_ метода **CreateMsgServiceEx,** значения _параметров ulUIParam_ и _ulFlags_ также передаются, когда называется функция точки входа службы сообщений. Поставщики служб должны отображать свои таблицы свойств конфигурации, чтобы пользователи могли настроить службу сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если аргумент **CreateMsgServiceEx** _lpuidService_ не является NULL, свойство PR_SERVICE_UID [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md)службы сообщений, добавленной в профиль, возвращается в **GUID,** на который указывает.  
  
Передай значение свойства **PR_SERVICE_UID** в  _параметре lpuidService_ [методу IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) для настройки службы. 
  
> [!CAUTION]
> Реализация Microsoft Outlook 2010, русская версия MAPI не поддерживает MAPI_UNICODE, если она используется. 
  
> [!IMPORTANT]
> Интерфейс IMsgServiceAdmin2 подвергается воздействию того же объекта, который реализует интерфейс IMsgServiceAdmin, и был доступен с Outlook реализации подсистемы MAPI с Outlook 2003 года. Его IID определяется следующим образом: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _ulFlags_ SERVICE_NO_RESTART_WARNING может не быть определен в загружаемом файле заголовки, который у вас есть в настоящее время, и в этом случае его можно добавить в код с помощью следующего значения: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>См. также



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

