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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Объект состояния поставщика транспорта можно использовать для изменения некоторых свойств поставщика. Диапазон свойств, которые можно изменить, зависит от свойств, включенных в таблицу свойств поставщика, и их определения. 
  
 **Перенастройка активного поставщика транспорта**
  
1. Вызов [IMAPISession::GetStatusTable для](imapisession-getstatustable.md) доступа к таблице состояния. 
    
2. Найдите строку для перенастройки поставщика транспорта, создав ограничение **свойства,** которое соответствует PR_DISPLAY_NAME ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)с именем целевого поставщика. 
    
3. Вызовите [IMAPITable::FindRow,](imapitable-findrow.md) чтобы получить соответствующую строку. 
    
4. Убедитесь, что STATUS_SETTINGS_DIALOG и STATUS_VALIDATE_STATE установлены в свойстве PR_RESOURCE_METHODS поставщика транспорта **(** [PidTagResourceMethods).](pidtagresourcemethods-canonical-property.md) Если STATUS_SETTINGS_DIALOG не заданная, поставщик транспорта не отображает таблицу свойств конфигурации. Если STATUS_VALIDATE_STATE не установлен, динамическую перенастройку выполнять нельзя.
    
5. Если STATUS_SETTINGS_DIALOG, вызовите [IMAPIStatus::SettingsDialog,](imapistatus-settingsdialog.md) чтобы отобразить лист свойств поставщика транспорта и разрешить пользователю вносить изменения. 
    
6. После завершения перенастройки пользователем вызовите [IMAPIStatus::ValidateState,](imapistatus-validatestate.md) если STATUS_VALIDATE_STATE настроен, передав CONFIG_CHANGED. 
    

