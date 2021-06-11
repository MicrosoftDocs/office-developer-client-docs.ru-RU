---
title: Перенастройка поставщика транспорта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408413"
---
# <a name="reconfiguring-a-transport-provider"></a>Перенастройка поставщика транспорта

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Вы можете использовать объект состояния поставщика транспорта, чтобы изменить некоторые свойства поставщика. Диапазон свойств, которые можно изменить, зависит от свойств, включенных в лист свойств поставщика, и от определения этих свойств. 
  
 **Перенастройка активного поставщика транспорта**
  
1. Вызов [IMAPISession::GetStatusTable,](imapisession-getstatustable.md) чтобы получить доступ к таблице состояния. 
    
2. Найдите строку для перенастройки поставщика транспорта, **создав** ограничение свойств, которое соответствует PR_DISPLAY_NAME [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)с именем целевого поставщика. 
    
3. Вызов [IMAPITable::FindRow,](imapitable-findrow.md) чтобы получить соответствующую строку. 
    
4. Убедитесь, что STATUS_SETTINGS_DIALOG и STATUS_VALIDATE_STATE в свойстве целевого поставщика транспорта **PR_RESOURCE_METHODS** [(PidTagResourceMethods).](pidtagresourcemethods-canonical-property.md) Если STATUS_SETTINGS_DIALOG не установлен, поставщик транспорта не отображает лист свойства конфигурации. Если STATUS_VALIDATE_STATE не установлено, динамическая перенастройка не выполняется.
    
5. Если STATUS_SETTINGS_DIALOG установлено, позвоните [в IMAPIStatus::SettingsDialog,](imapistatus-settingsdialog.md) чтобы отобразить лист свойств поставщика транспорта и разрешить пользователю вносить изменения. 
    
6. После завершения перенастройки пользователем позвоните [в IMAPIStatus::ValidateState,](imapistatus-validatestate.md) если STATUS_VALIDATE_STATE установлено, CONFIG_CHANGED. 
    

