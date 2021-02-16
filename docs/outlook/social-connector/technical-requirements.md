---
title: Технические требования
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: В этом разделе описываются поддерживаемые языки программирования, требования к типу видимости COM и возвращаемого метода, а также сведения о DLL-коде для возможности extensibility поставщика Outlook Social Connector (OSC).
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329157"
---
# <a name="technical-requirements"></a>Технические требования

В этом разделе описываются поддерживаемые языки программирования, требования к типу видимости COM и возвращаемого метода, а также сведения о DLL extensibility поставщика Outlook Social Connector (OSC). 
  
## <a name="programming-language-and-com-requirements"></a>Язык программирования и требования COM

Вы можете создать поставщика OSC с помощью управляемых языков, таких как Visual C# или Visual Basic, или неугодных языков, таких как Visual C++. Для разработки поставщика OSC можно использовать любое средство, которое может создать компонент DLL, видимый com. При принятии решения об использовании управляемого или неугодного языка для разработки поставщика следует учитывать размер скачивания и зависимости пакета установки поставщика.
  
Поставщик OSC должен быть видимым com, как определено в следующих данных:
  
- После установки поставщик OSC должен быть зарегистрирован с помощью самостоятельной регистрации COM или regsvr32.
    
- Регистрация DLL поставщика OSC com регистрирует поставщика в HKCU или HKLM. 
    
- ProgID поставщика зарегистрирован в  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` .
    
- Поставщик OSC, разработанный на управляемом языке, виден COM.
    
- Поставщик OSC должен добавить в реестр Windows значения, которые указывают, что DLL поставщика поддерживает однопоточная модель однопотоковой однопотоковой многопоточной модели многопотоковых многопотоковых окон (MTA). Дополнительные сведения о моделях потоков COM см. в описании и работе моделей [потоков OLE.](https://support.microsoft.com/kb/150777)
    
Методы в extensibility поставщика OSC должны возвращать примитивные типы, такие как **строка** или **bool.** Некоторые  возвращаемые строки должны соответствовать определению схемы для возможности extensibility поставщика OSC. В качестве возвращаемой величины поддерживается только XML. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Сведения о DLL для extensibility поставщика OSC

Компонентом, который поддерживает возможности extensibility поставщика OSC, является DLL для extensibility поставщика OSC. Сторонние разработчики могут создавать DLL поставщика OSC с помощью этих интерфейсов. В следующем списке показаны сведения о DLL для extensibility поставщика OSC:
  
- Имя файла DLL для extensibility: socialprovider.dll
    
- Удобное имя DLL для extensibility: Microsoft Outlook Social Provider Extensibility
    
- Основная версия DLL для extensibility: 15.0
    
- Extensibiilty DLL TypeLib, версия: 1.1
    
## <a name="miscellaneous-technical-information"></a>Прочие технические сведения

Нотация объектов JavaScript (JSON) не поддерживается в модели extensibility поставщика OSC.
  
Нет зависимостей от синтаксической разбиения XML. Поставщик OSC может использовать синтаксическая программа синтаксики XML, включаемая в Office, например MSXML (MSXML), использовать возможности синтаксики XML, встроенные в Microsoft .NET Framework, или сторонний синтаксик XML. 
  
## <a name="see-also"></a>См. также

- [Best Practices for Developing a Provider](best-practices-for-developing-a-provider.md)  
- [Быстрые шаги по обучению разработке поставщика](quick-steps-for-learning-to-develop-a-provider.md)
- [Развертывание поставщика](deploying-a-provider.md)  
- [Начало разработки поставщика Outlook Social Connector](getting-started-with-developing-an-outlook-social-connector-provider.md)

