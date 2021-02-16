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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Если вы решили написать код для создания профиля, убедитесь, что вы понимаете, как заказать записи профиля, а также тип и объем информации, необходимый для каждой записи. Результаты упорядочения записей в профиле поясняется в [профилях MAPI.](mapi-profiles.md)
  
 **Создание профиля с кодом C или C++**
  
1. Прочитайте файл загона для каждой службы сообщений. В этой теме поймут, какие свойства необходимо настроить и какие значения будут использовать.
    
2. Вызовите [функцию MAPIAdminProfiles,](mapiadminprofiles.md) чтобы получить указатель интерфейса **IProfAdmin.** 
    
3. Вызовите [IProfAdmin::CreateProfile,](iprofadmin-createprofile.md) чтобы создать профиль. Если вы хотите создать профиль со службами сообщений, перечисленными в разделе **[Службы** по умолчанию] MAPISVC. INF-файл, установите флаг MAPI_DEFAULT_SERVICE. Если вы хотите включить для пользователя ввод сведений о конфигурации, установите MAPI_DIALOG флага. Убедитесь, что этот флаг установлен, если не все необходимые сведения доступны через MAPISVC. INF-файл. **CreateProfile** вызывает функцию точки входа для каждой службы сообщений, добавляемой в профиль с MSG_SERVICE_CREATE в качестве параметра _ulContext._ 
    
4. Вызовите [IProfAdmin::AdminServices,](iprofadmin-adminservices.md) чтобы получить объект администрирования службы сообщений. 
    
5. Используйте объект администрирования службы сообщений для добавления служб сообщений в профиль. Для каждой службы сообщений, которую вы хотите добавить:
    
1. Вызовите [метод IMsgServiceAdmin::CreateMsgService,](imsgserviceadmin-createmsgservice.md) чтобы создать новую службу сообщений. 
    
2. Вызовите [IMsgServiceAdmin::ConfigureMsgService,](imsgserviceadmin-configuremsgservice.md)передав структуру **MAPIUID** только что созданной службы и массив значений свойств со свойствами конфигурации. 
    
6. Чтобы получить идентификатор только что добавленной службы, который является ее свойством **PR_SERVICE_UID** ([PidTagServiceUid),](pidtagserviceuid-canonical-property.md)вызовите [IMsgServiceAdmin::GetMsgServiceTable,](imsgserviceadmin-getmsgservicetable.md) чтобы получить доступ к таблице службы сообщений и найти строку, которая представляет службу сообщений. Последняя строка в таблице представляет последнюю добавленную службу сообщений. 
    
Чтобы сделать новый профиль временным, вызовите метод [IProfAdmin::D eleteProfile](iprofadmin-deleteprofile.md) сразу после входа. **DeleteProfile** пометит новый профиль как удаленный во время его работы в течение сеанса. Так как она не будет включена в таблицу профилей сеанса, другие клиенты не смогут использовать ее. 
  

