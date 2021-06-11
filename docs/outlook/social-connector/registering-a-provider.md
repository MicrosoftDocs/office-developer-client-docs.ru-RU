---
title: Регистрация поставщика
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: В этом разделе описываются Windows реестра, которые используются при установке поставщика Outlook social Connector (OSC).
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421762"
---
# <a name="registering-a-provider"></a>Регистрация поставщика

В этом разделе описываются Windows реестра, которые используются при установке поставщика Outlook social Connector (OSC).
  
## <a name="com-registration"></a>Регистрация COM

Необходимо настроить DLL поставщика OSC для регистрации с помощью саморегистрации COM или regsvr32 во время установки. Регистрация com поставщика DLL регистрирует поставщика OSC в `HKEY_CLASSES_ROOT` улье реестра. 
  
Поставщик OSC, разработанный в управляемом коде, имеет сборку поставщика с видимыми com-кодами. Для компонента поставщика следует использовать отдельный домен приложения. В противном случае поставщик OSC использует домен общего приложения по умолчанию, используемый другими компонентами, и поставщик может работать не так, как ожидалось.
  
## <a name="registering-provider-progid"></a>Поставщик регистрации ProgID

Каждый поставщик OSC должен зарегистрировать программный идентификатор ( `ProgID` ). Установщик поставщика может выбрать одно из следующих местоположений, чтобы добавить или `ProgID` удалить:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`Установщик поставщика должен использовать это расположение, если поставщик установлен только для зарегистрированного в настоящее время &ndash; пользователя.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`Установщик поставщика должен использовать это расположение, если поставщик установлен &ndash; для всех пользователей на компьютере.
    
OsC ищет поставщика в вышеуказанных расположениях, если клиентский компьютер не имеет `ProgID` 32-Outlook на 64-Windows операционной системе. В этом случае установщик поставщика должен выбрать одно из следующих местоположений в  `HKEY_CURRENT_USER`  `HKEY_LOCAL_MACHINE` улье или в улье: 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Для мышиной версии Office установщик поставщика должен выбрать одно из следующих местоположений в HKEY_CURRENT_USER или HKEY_LOCAL_MACHINE улье:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>См. также

- [Контрольный список установки](installation-checklist.md)
- [Быстрые шаги для обучения разработке поставщика](quick-steps-for-learning-to-develop-a-provider.md)
- [Развертывание поставщика](deploying-a-provider.md)

