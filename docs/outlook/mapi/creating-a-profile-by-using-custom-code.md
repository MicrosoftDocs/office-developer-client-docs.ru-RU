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
ms.openlocfilehash: f3270528194b3cc3429d3afec153355349dabbff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413306"
---
# <a name="creating-a-profile-by-using-custom-code"></a>Создание профиля с помощью пользовательского кода

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Если вы решите написать код для создания профиля, убедитесь, что вы понимаете, как заказать записи профилей, а также тип и объем информации, необходимый для каждой записи. Последствия заказа записей в профиле объясняются в [профилях MAPI.](mapi-profiles.md)
  
 **Создание профиля с кодом C или C++**
  
1. Ознакомьтесь с файлом загона для каждой службы сообщений. Поймите, какие свойства необходимо настроить и какие значения вы будете использовать.
    
2. Вызов [функции MAPIAdminProfiles](mapiadminprofiles.md) для получения указателя интерфейса **IProfAdmin.** 
    
3. Вызов [IProfAdmin::CreateProfile](iprofadmin-createprofile.md) для создания профиля. Если вы хотите создать профиль со службами сообщений, перечисленными в **разделе [Службы** по умолчанию] MAPISVC. Файл INF, установите флаг MAPI_DEFAULT_SERVICE. Если вы хотите включить пользователю ввод сведений о конфигурации, установите флаг MAPI_DIALOG. Убедитесь, что этот флаг установлен, если не вся необходимая информация доступна через MAPISVC. Файл INF. **CreateProfile** вызывает функцию точки входа для каждой службы сообщений, которая будет добавлена в профиль с MSG_SERVICE_CREATE в качестве _параметра ulContext._ 
    
4. Вызов [IProfAdmin::AdminServices для](iprofadmin-adminservices.md) получения объекта администрирования службы сообщений. 
    
5. Используйте объект администрирования служб сообщений, чтобы добавить службы сообщений в профиль. Для каждой службы сообщений, которую необходимо добавить:
    
1. Вызов метода [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) для создания новой службы сообщений. 
    
2. Вызов [IMsgServiceAdmin::ConfigureMsgService,](imsgserviceadmin-configuremsgservice.md)передав структуру **MAPIUID** только что созданной службы и массив свойств со свойствами конфигурации. 
    
6. Чтобы получить идентификатор недавно добавленной **службы,** которая является ее свойством [PR_SERVICE_UID (PidTagServiceUid),](pidtagserviceuid-canonical-property.md)позвоните [в службу IMsgServiceAdmin::GetMsgServiceTable,](imsgserviceadmin-getmsgservicetable.md) чтобы получить доступ к таблице службы сообщений и поиска строки, представляющем службу сообщений. Последняя строка в таблице будет представлять последнюю добавленную службу сообщений. 
    
Чтобы сделать новый профиль временным, немедленно после входа вызывайте метод [IProfAdmin::D eleteProfile.](iprofadmin-deleteprofile.md) **DeleteProfile** будет отмечать новый профиль как удаленный, делая его годным для работы в течение сеанса. Так как она не будет включена в таблицу профилей сеанса, другие клиенты не смогут ее использовать. 
  

