---
title: Создание профиля с помощью пользовательского кода
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5632cd25-58f5-4b9c-906c-cd377abc3daf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c14d58e8a03633615798b50b256b9cc54fcc4f4c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594735"
---
# <a name="creating-a-profile-by-using-custom-code"></a>Создание профиля с помощью пользовательского кода

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Если вы решаете написать код, чтобы создать профиль, убедитесь в том, что вам понять, как порядок записи профиля и тип и объем сведений, необходимых для каждой записи. Влияние на порядок записей в профиле объясняется [Профили MAPI](mapi-profiles.md).
  
 **Чтобы создать профиль с помощью кода C или C++**
  
1. Чтение файла заголовка для каждой службы сообщений. Понять, какие свойства, необходимо будет настроить и какие значения, которое будет использоваться.
    
2. Вызовите функцию [MAPIAdminProfiles](mapiadminprofiles.md) для получения указателя интерфейса **IProfAdmin** . 
    
3. Вызов [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) для создания профиля. Если вы хотите создать профиль с помощью службы сообщений, перечисленных в разделе **[Службы по умолчанию]** файл Mapisvc.inf. INF-файл, задайте флаг MAPI_DEFAULT_SERVICE. Чтобы разрешить пользователю требуется ввести сведения о конфигурации, установите флажок MAPI_DIALOG. Убедитесь в том, что установить этот флажок, если не все необходимые сведения, доступные через файл Mapisvc.inf. INF-файл. **CreateProfile** вызывает функцию точки входа для каждой службы сообщения добавляется к профилю с MSG_SERVICE_CREATE установите в качестве параметра _ulContext_ . 
    
4. Вызовите [IProfAdmin::AdminServices](iprofadmin-adminservices.md) , чтобы получить объект администрирования службы сообщений. 
    
5. Используйте объект администрирования службы сообщений для добавления службы сообщений к профилю. Для каждой службы сообщение, которое вы хотите добавить:
    
1. Вызовите метод [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) для создания новой службы сообщений. 
    
2. Вызовите [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md), передав структура **MAPIUID** службу, которую вы только что создали и массива значение свойства с помощью его свойства конфигурации. 
    
6. Для получения идентификатора новые службы, которая его свойство **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)), вызовите [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) для доступа к таблице службы сообщений и поиск строку, представляющую Служба сообщений. Последняя строка в таблице будет представлять недавно добавлены службы сообщений. 
    
Чтобы выбрать новый профиль временный, вызовите метод [IProfAdmin::DeleteProfile](iprofadmin-deleteprofile.md) сразу же после входа в систему. **DeleteProfile** будут помечены новый профиль, как удаленное при выполнении можно использовать во время сеанса. Так как он не будет включаться в таблице профилей сеанса, других клиентов будет невозможно использовать его. 
  

