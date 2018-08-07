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
ms.openlocfilehash: 6e0bdd7108bacd17134592ac05ba71510fde76d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809388"
---
# <a name="imsgserviceadmincreatemsgservice"></a>IMsgServiceAdmin::CreateMsgService

  
  
**Относится к**: Outlook 
  
Устаревшие: Рекомендуется использовать [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) . Добавление службы сообщений для текущего профиля. 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
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
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NOT_FOUND 
  
> Имя службы сообщение не является в разделе **[Services]** MapiSvc.inf. 
    
## <a name="remarks"></a>Замечания

Метод **IMsgServiceAdmin::CreateMsgService** добавляет службы сообщений для текущего профиля. **CreateMsgService** вызывает функцию точки входа службы сообщений для выполнения каких-либо задач конфигурации службы. Если в параметре _ulFlags_ флаг SERVICE_UI_ALLOWED, устанавливаемой службы сообщений можно отобразить страницу свойств, чтобы разрешить пользователю настраивать его параметры. 
  
Файла MapiSvc.inf содержит список поставщиков, которые составляют службы сообщений и свойства для каждого из них. **CreateMsgService** сначала создается новый раздел профиля для службы сообщений и затем копирует все данные для этой службы из файла MapiSvc.inf в профиль, создание новых раздела для каждого поставщика. 
  
После копирования всей информации из MapiSvc.inf функции точки входа службы сообщений вызывается с MSG_SERVICE_CREATE значение, установленное в параметре _ulContext_ . Если флаг SERVICE_UI_ALLOWED установлен в параметре _ulFlags_ метод **CreateMsgService** , в параметрах _ulUIParam_ и _ulFlags_ также передаются значения при вызове функции точки входа службы сообщений. Поставщиков услуг должны отображать свойств их конфигурации, поэтому пользователи могут настраивать службы сообщений. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **CreateMsgService** не возвращает структуру [MAPIUID](mapiuid.md) для службы сообщений, который был добавлен к профилю. 
  
Чтобы получить **MAPIUID** сообщение о создании службы, используйте следующую процедуру: 
  
1. Вызовите метод [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) для получения таблицы администрирования службы сообщений. 
    
2. Найдите строку, которая представляет службы сообщений, установив ограничение в таблице, которая соответствует свойству **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) с именем службы сообщений. 
    
3. Получение свойств службы **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)). 
    
4. Передайте значение свойства **PR_SERVICE_UID** с помощью параметра _lpUid_ методу [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , чтобы настроить службу. 
    
> [!CAUTION]
> Реализация Microsoft Outlook 2010 подсистемы MAPI не поддерживает MAPI_UNICODE и завершится ошибкой, если она используется. 
  
> [!IMPORTANT]
> _UlFlags_ SERVICE_NO_RESTART_WARNING не могут быть определены в файле загружаемых заголовка в настоящий момент, в этом случае можно добавить его в код с помощью следующее значение: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |Mfcmapi (en) использует метод **IMsgServiceAdmin::CreateMsgService** для добавления в профиль службы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

