---
title: Поиск имени профиля
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b4efdd8d8238d4bc7e89a1153b9be34c7af76355
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407923"
---
# <a name="finding-a-profile-name"></a>Поиск имени профиля

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Иногда клиентам необходимо найти имя профиля, используемого в данный момент для сеанса, имя профиля по умолчанию или имя альтернативного профиля, установленного на компьютере.
  
Существует несколько способов извлечения имени профиля во время сеанса. Если необходимо найти имя профиля, который не обязательно используется для сеанса, используйте первую процедуру. Если вам нужно найти имя профиля по умолчанию, используйте вторую процедуру. Если вам нужно найти имя текущего профиля для сеанса, используйте последнюю процедуру. 
  
 **Поиск имени любого профиля**
  
1. Вызовите [мапиадминпрофилес](mapiadminprofiles.md) , чтобы получить указатель интерфейса **ипрофадмин** . 
    
2. Call [ипрофадмин:: жетпрофилетабле](iprofadmin-getprofiletable.md) для доступа к таблице профилей. 
    
3. Вызовите таблицу профилей [IMAPITable:: QueryRows](imapitable-queryrows.md) , чтобы получить все строки в таблице и проверить каждую из них, чтобы определить, соответствует ли она целевому профилю. 
    
 **Поиск имени профиля по умолчанию**
  
1. Вызовите [мапиадминпрофилес](mapiadminprofiles.md).
    
2. Call [ипрофадмин:: жетпрофилетабле](iprofadmin-getprofiletable.md) для доступа к таблице профилей. 
    
3. Создайте ограничение свойства с помощью структуры [спропертирестриктион](spropertyrestriction.md) для сравнения **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) со значением true.
    
4. Call [IMAPITable:: FindRow](imapitable-findrow.md) для обнаружения строки в таблице Profile, которая представляет профиль по умолчанию. Столбец **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) содержит имя профиля по умолчанию.
    
 **Поиск имени текущего профиля**
  
Чтобы найти имя текущего профиля, выполните одно из указанных ниже действий.
  
- Предполагается, что структура [мапиуид](mapiuid.md) , представляющая один из разделов текущего профиля, передается в параметре _лпуид_ в [IMAPISession:: опенпрофилесектион](imapisession-openprofilesection.md). Получите свойство **PR_PROFILE_NAME** раздела профиля ([PidTagProfileName](pidtagprofilename-canonical-property.md)) с помощью метода [IMAPIProp::-PROPS](imapiprop-getprops.md) . 
    
- Call [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для доступа к таблице status и поиска строки, в которой для столбца **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) задано значение MAPI_SUBSYSTEM. Столбец **PR_DISPLAY_NAME** для этой строки является именем профиля. Не используйте таблицу Status во время запуска, так как она блокирует приложение до тех пор, пока диспетчер очереди MAPI не завершит инициализацию всех поставщиков транспорта. Это может привести к снижению производительности. 
    

