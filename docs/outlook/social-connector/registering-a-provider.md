---
title: Регистрация поставщика
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: В этом разделе описываются расположения реестра Windows, используемые при установке поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329213"
---
# <a name="registering-a-provider"></a>Регистрация поставщика

В этом разделе описываются расположения реестра Windows, используемые при установке поставщика Outlook Social Connector (OSC).
  
## <a name="com-registration"></a>Регистрация COM

Необходимо настроить БИБЛИОТЕКУ DLL поставщика OSC для регистрации с помощью функции самостоятельной регистрации COM или regsvr32 во время установки. Регистрация в COM для библиотеки DLL поставщика регистрирует поставщика OSC в кусте `HKEY_CLASSES_ROOT` реестра. 
  
Поставщик OSC, разработанный в управляемом коде, имеет сборку поставщика, видимую для COM. Для компонента поставщика следует использовать отдельный домен приложения. В противном случае поставщик OSC использует общий домен приложения по умолчанию, который используется другими компонентами, и поставщик может работать не так, как ожидалось.
  
## <a name="registering-provider-progid"></a>Регистрация ProgID поставщика

Каждый поставщик OSC должен зарегистрировать программный идентификатор (`ProgID`). Установщик поставщика может выбрать одно из следующих расположений, `ProgID`чтобы добавить или удалить:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Установщик поставщика должен использовать это расположение, если поставщик установлен только для пользователя, выполнившего вход в систему.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Установщик поставщика должен использовать это расположение, если поставщик установлен для всех пользователей компьютера.
    
OSC ищет поставщика `ProgID` в указанных выше расположениях, если на клиентском компьютере не установлено приложение 32 (в том случае, если на нем работает приложение в 64 — более разрядная версия операционной системы Windows. В этом случае установщик поставщика должен выбрать одно из следующих расположений в кусте `HKEY_CURRENT_USER` или `HKEY_LOCAL_MACHINE` кусте: 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Для версии Office "нажми и работай" установщик поставщика должен выбрать одно из следующих расположений в кусте HKEY_CURRENT_USER или HKEY_LOCAL_MACHINE:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>См. также

- [Контрольный список установки](installation-checklist.md)
- [Быстрые действия для изучения разработки поставщика](quick-steps-for-learning-to-develop-a-provider.md)
- [Развертывание поставщика](deploying-a-provider.md)

