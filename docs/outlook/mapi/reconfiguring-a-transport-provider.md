---
title: Изменение конфигурации поставщика транспорта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5e7c94b387a5fe9f9682854de4097f6f1bbcd786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565601"
---
# <a name="reconfiguring-a-transport-provider"></a>Изменение конфигурации поставщика транспорта

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Чтобы изменить некоторые свойства поставщика можно использовать объект состояние поставщика транспорта. Диапазон свойств, которые могут быть изменены зависит от свойства, которые включены в поставщика свойств и определение этих свойств. 
  
 **Чтобы снова настроить поставщика транспорта активный**
  
1. Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к таблице состояния. 
    
2. Найдите строку для поставщика транспорта нужно правильно настроить путем создания ограничение свойство, которое соответствует **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) с именем конечного поставщика. 
    
3. Вызов [IMAPITable::FindRow](imapitable-findrow.md) для извлечения соответствующих строк. 
    
4. Проверьте, что в свойстве **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)), поставщика транспорта конечного флаги STATUS_SETTINGS_DIALOG и STATUS_VALIDATE_STATE. Если STATUS_SETTINGS_DIALOG не задано, поставщика транспорта не отображаются на листе свойств конфигурации. Если STATUS_VALIDATE_STATE не задано, не может выполнять динамической перенастройки.
    
5. Если значение STATUS_SETTINGS_DIALOG, вызовите [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) , чтобы открыть окно свойств поставщика транспорта и пользователи могут вносить изменения. 
    
6. По окончании пользователя с перенастроить вызовите [IMAPIStatus::ValidateState](imapistatus-validatestate.md) , если задано STATUS_VALIDATE_STATE, передав CONFIG_CHANGED. 
    

