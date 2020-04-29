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
  
Вы можете использовать объект состояния поставщика транспорта, чтобы изменить некоторые свойства поставщика. Диапазон свойств, которые можно изменить, зависит от свойств, которые включены в страницу свойств поставщика, и от того, как эти свойства определены. 
  
 **Повторная настройка активного поставщика транспорта**
  
1. Call [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для доступа к таблице состояния. 
    
2. Укажите строку для поставщика транспорта, которую необходимо изменить, создав ограничение свойства, которое соответствует **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) с именем целевого поставщика. 
    
3. Call [IMAPITable:: FindRow](imapitable-findrow.md) для получения соответствующей строки. 
    
4. Убедитесь, что флаги STATUS_SETTINGS_DIALOG и STATUS_VALIDATE_STATE заданы в свойстве **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) целевого поставщика транспорта. Если STATUS_SETTINGS_DIALOG не задано, то поставщик транспорта не отображает страницу свойств конфигурации. Если STATUS_VALIDATE_STATE не задано, то невозможно выполнить динамическую перенастройку.
    
5. Если параметр STATUS_SETTINGS_DIALOG задан, вызовите метод [имапистатус:: сеттингсдиалог](imapistatus-settingsdialog.md) , чтобы отобразить лист свойств поставщика транспорта и разрешить пользователю вносить изменения. 
    
6. После завершения перенастройки вызовите метод [имапистатус:: валидатестате](imapistatus-validatestate.md) , если STATUS_VALIDATE_STATE задан, передавая CONFIG_CHANGED. 
    

