---
title: Поддержка инструмента iOS Document Picker в Office для iOS
manager: soliver
ms.date: 02/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 802224ef-6eea-4929-824c-507da1c073a5
description: Office для iOS можно интегрировать с инструментом iOS Document Picker с помощью расширения Document Provider, что позволит Office открывать файлы, хранящиеся у другого поставщика документов.
ms.openlocfilehash: e3a3374c7fd33bb00ed076075eb6199c24eec923
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410667"
---
# <a name="office-for-ios-support-for-the-ios-document-picker"></a>Поддержка инструмента iOS Document Picker в Office для iOS

Office для iOS можно интегрировать с инструментом iOS Document Picker с помощью расширения Document Provider, что позволит Office открывать файлы, хранящиеся у другого поставщика документов.
  
Версии ОС iOS от компании Apple, начиная с iOS 8.0, предусматривают [поддержку расширений приложений](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1). Вы можете использовать эти расширения, чтобы интегрировать функции своего приложения в другие приложения или среды на устройстве пользователя. Чтобы интегрировать Office для iOS и инструмент iOS Document Picker, используйте [расширение Document Provider](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html).
  
Расширение Document Provider поддерживает четыре операции:
  
- Импорт
    
- Экспорт
    
- Открытие
    
- Перемещение
    
При интеграции Office для iOS доступна операция открытия. После создания расширения Document Provider пользователи могут использовать инструмент Document Picker, чтобы открывать и редактировать документы непосредственно в Office, не создавая копию файла.
  
## <a name="learn-more-about-app-extensions-and-the-document-picker"></a>Дополнительные сведения о расширениях приложений и инструменте Document Picker
<a name="bk_addresources"> </a>

- [Расширения приложений](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/index.html#//apple_ref/doc/uid/TP40014214-CH20-SW1)
    
- [Руководство по программированию, касающееся Document Picker](https://developer.apple.com/library/prerelease/ios/documentation/FileManagement/Conceptual/DocumentPickerProgrammingGuide/Introduction/Introduction.html)
    
- [Руководство по программированию, касающееся Document Provider](https://developer.apple.com/library/prerelease/ios/documentation/General/Conceptual/ExtensibilityPG/FileProvider.html)
    

