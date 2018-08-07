---
title: Регистрация поставщика
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: В этом разделе описываются разделах реестра Windows, которые используются при установке поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 3ec594ec94b045d2ceb583144781a5746b945b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812829"
---
# <a name="registering-a-provider"></a>Регистрация поставщика

В этом разделе описываются разделах реестра Windows, которые используются при установке поставщика Outlook Social Connector (OSC).
  
## <a name="com-registration"></a>Регистрация COM

Необходимо настроить поставщика OSC DLL-Библиотеку для регистрации с помощью COM самостоятельной регистрации или regsvr32 во время установки. Регистрация COM DLL-Библиотеки поставщика регистрируется поставщик OSC в разделе `HKEY_CLASSES_ROOT` куст реестра. 
  
Поставщика OSC, разработанных в управляемом коде имеет COM-видимым сборки поставщика. Следует использовать отдельного домена приложений для компонента поставщика. В противном случае поставщика OSC использует домен общего приложения по умолчанию, используемый с другими компонентами и поставщик может не работать нормально.
  
## <a name="registering-provider-progid"></a>Регистрация поставщика ProgID

Каждый поставщик OSC необходимо зарегистрировать программный идентификатор (`ProgID`). Установщик поставщика можно выбрать один из следующих расположений для добавления или удаления `ProgID`:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Установщик поставщика следует использовать это расположение, если поставщик устанавливается только для текущего пользователя.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Установщик поставщика следует использовать это расположение поставщик в случае установки для всех пользователей на компьютере.
    
Находит поставщика OSC `ProgID` в вышеуказанных местах, только при наличии 32-разрядная версия Outlook при работе на 64-разрядной операционной системы Windows на клиентском компьютере. В этом случае установщик поставщик должен выбрать один из следующих расположений в `HKEY_CURRENT_USER` или `HKEY_LOCAL_MACHINE` куст: 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Click-to-Run версии системы Office установщик поставщик должен выбрать один из следующих расположений в кусте HKEY_CURRENT_USER или HKEY_LOCAL_MACHINE:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>См. также

- [Контрольный список установки](installation-checklist.md)
- [Быстрый шаги, необходимые для разработки поставщика](quick-steps-for-learning-to-develop-a-provider.md)
- [Развертывание поставщика](deploying-a-provider.md)

