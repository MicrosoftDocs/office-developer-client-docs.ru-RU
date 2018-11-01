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
ms.openlocfilehash: f700389315ca7bd184a9d6defb0b44eaec99a38e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574778"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Добавление службы сообщений для текущего профиля и возвращает, недавно добавленных службы ИД пользователя.
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a>Параметры

 _lpszService_
  
> [in] Указатель на имя службы сообщений для добавления. Это имя службы сообщений, которые должны встречаться в разделе **[Services]** файла MapiSvc.inf. 
    
 _lpszDisplayName_
  
> [in] Указатель на отображаемое имя службы сообщений для добавления. Параметр _lpszDisplayName_ игнорируется, если служба сообщений значение свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) в файле MapiSvc.inf.
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна из диалоговых окон и windows отображает этот метод.
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет способ установки службы сообщений. Можно задать следующие флажки:
    
MAPI_UNICODE
  
> Параметры lpszDisplayName и lpszService должен привести к LPWSTR и как строк в кодировке Юникод.
    
SERVICE_NO_RESTART_WARNING
  
> При добавлении нового сообщения службы профиля, подсистема MAPI на основе различных ситуациях и условия, часто определяет, что это действие требуется для Outlook. Если флаг SERVICE_NO_RESTART_WARNING не указан и может пользовательского интерфейса — в зависимости от флаги SERVICE_UI_ALWAYS и SERVICE_UI_ALLOWED - и по крайней мере один процесс выполнил вход в систему текущего профиля, эта функция отображает сообщение «необходимо перезапустить Outlook для Эти изменения вступили в силу.» Включая флаг SERVICE_NO_RESTART_WARNING подавляет, сообщение с предупреждением.
    
SERVICE_UI_ALLOWED
  
> Конфигурация службы сообщения пользовательского интерфейса может при необходимости.
    
SERVICE_UI_ALWAYS
  
> Служба сообщений отображается окно свойств конфигурации.
    
 _lpuidService_
  
> [out] Указатель на UID добавлена служба сообщений.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NOT_FOUND
  
> Имя службы сообщение не является в разделе **[Services]** MapiSvc.inf. 
    
## <a name="remarks"></a>Замечания

Метод **IMsgServiceAdmin2::CreateMsgServiceEx** добавляет службы сообщений для текущего профиля. **CreateMsgServiceEx** вызывает функцию точки входа службы сообщений для выполнения каких-либо задач конфигурации службы. Если в параметре _ulFlags_ флаг SERVICE_UI_ALLOWED, устанавливаемой службы сообщений можно отобразить страницу свойств, позволяя пользователям для настройки ее параметров. 
  
Файла MapiSvc.inf содержит список поставщиков, которые составляют службы сообщений и свойства для каждого из них. **CreateMsgServiceEx** сначала создается новый раздел профиля для службы сообщений и затем копирует все данные для этой службы из файла MapiSvc.inf в профиль, создание новых раздела для каждого поставщика. 
  
После копирования всей информации из MapiSvc.inf функцию точки входа для службы сообщений, **MSGSERVICEENTRY**вызывается с MSG_SERVICE_CREATE значение, установленное в параметре _ulContext_ . Если флаг SERVICE_UI_ALLOWED установлен в параметре _ulFlags_ метод **CreateMsgServiceEx** , в параметрах _ulUIParam_ и _ulFlags_ также передаются значения при вызове функции точки входа службы сообщений. Поставщиков услуг должны отображать свойств их конфигурации, поэтому пользователи могут настраивать службы сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Если аргумент _lpuidService_ **CreateMsgServiceEx** не может быть NULL, свойство **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) службы сообщений, который был добавлен к профилю возвращается **идентификатор GUID** , на который указывает. 
  
Передайте значение свойства **PR_SERVICE_UID** с помощью параметра _lpuidService_ методу [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , чтобы настроить службу. 
  
> [!CAUTION]
> Реализация Microsoft Outlook 2010 подсистемы MAPI не поддерживает MAPI_UNICODE и завершится ошибкой, если она используется. 
  
> [!IMPORTANT]
> Интерфейс IMsgServiceAdmin2 предоставляется тот же объект, который реализует интерфейс IMsgServiceAdmin и уже была доступна с помощью Outlook реализации подсистемы MAPI, начиная с Outlook 2003. ИД его интерфейса определяется следующим образом: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _ulFlags_ SERVICE_NO_RESTART_WARNING не могут быть определены в файле загружаемых заголовка в настоящий момент, в этом случае можно добавить его в код с помощью следующее значение: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>См. также



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

