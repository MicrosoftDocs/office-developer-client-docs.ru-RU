---
title: Технические требования
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eff6d5d6-8855-4e54-a781-9deab8cc0aca
description: В этом разделе описываются поддерживаемые языки программирования, требования к типам возврата com и возвращаемого метода, а также сведения о Outlook поставщике Outlook поставщике extensibility DLL.
ms.openlocfilehash: 14dfcf52d714177775c5610b5da91d174f81a132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329157"
---
# <a name="technical-requirements"></a>Технические требования

В этом разделе описываются поддерживаемые языки программирования, требования к типам возврата com и возвращаемого метода, а также сведения о Outlook поставщике Outlook поставщике extensibility DLL. 
  
## <a name="programming-language-and-com-requirements"></a>Язык программирования и требования com

Вы можете создать поставщика OSC с помощью управляемых языков, таких как Visual C# или Visual Basic, или неугодных языков, таких как Visual C++. Для разработки поставщика OSC можно использовать любой инструмент, который может создать компонент DLL, видимый в COM. При решении использовать управляемый или неустановимый язык для разработки поставщика следует учитывать размер загрузки и зависимости пакета установки поставщика.
  
Поставщик OSC должен быть com-видимым в соответствии со следующими следующими словами:
  
- После установки поставщик OSC должен быть зарегистрирован с помощью самостоятельной регистрации COM или regsvr32.
    
- Регистрация поставщика поставщиков OSC DLL регистрирует поставщика в HKCU или HKLM. 
    
- ProgID поставщика регистрируется под  `HKCU\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` .
    
- Поставщик OSC, разработанный на управляемом языке, является com-видимым.
    
- Поставщик OSC должен добавить значения в реестр Windows, которые указывают на то, что поставщик DLL поддерживает как однопотовые модели потоков квартиры (STA) так и многопотоковые модели потоков квартиры (MTA). Дополнительные сведения о моделях потоков com см. в описании и [работе моделей потоков OLE.](https://support.microsoft.com/kb/150777)
    
Методы в extensibility поставщика OSC должны возвращать примитивные типы, такие как **строка** **или бол.** Некоторые **значения возврата** строки должны соответствовать определению схемы для extensibility поставщика OSC. Только XML поддерживается как возвращаемая величина. 
  
## <a name="details-of-the-osc-provider-extensibility-dll"></a>Сведения о поставщике extensibility DLL поставщика OSC

Компонент, который поддерживает удлиняемость поставщика OSC, — это DLL поставщика extensibility OSC. Сторонние разработчики могут создавать DLL-интерфейсы поставщика OSC с помощью этих интерфейсов. В следующем списке показаны сведения о DLL поставщика extensibility osC:
  
- Имя файла DLL: socialprovider.dll
    
- Удобное имя DLL: Microsoft Outlook для социальных поставщиков
    
- Основная версия DLL: 15.0
    
- Extensibiilty DLL TypeLib версии: 1.1
    
## <a name="miscellaneous-technical-information"></a>Различные технические сведения

Нотация объектов JavaScript (JSON) не поддерживается в модели extensibility поставщика OSC.
  
Нет зависимостей от XML-parser. Поставщик OSC может использовать XML-parser, включенный в Office, например MSXML (MSXML), использовать возможности XML-разреза, встроенные в microsoft платформа .NET Framework, или использовать сторонний синтаксик XML. 
  
## <a name="see-also"></a>См. также

- [Лучшие практики для разработки поставщика](best-practices-for-developing-a-provider.md)  
- [Быстрые шаги для обучения разработке поставщика](quick-steps-for-learning-to-develop-a-provider.md)
- [Развертывание поставщика](deploying-a-provider.md)  
- [Начало работы с разработкой Outlook поставщика социальных соединители](getting-started-with-developing-an-outlook-social-connector-provider.md)

