---
title: Проверка подлинности на основе форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 282b2377-45ba-4f0c-a7d9-830fa3505c93
description: 'Outlook Social Connector (OSC) вызывает метод ИсоЦиалпровидер:: capabilities, который определяет возможности поставщика OSC для социальной сети.'
ms.openlocfilehash: 420f19a8d7632f2ab9b093eb929ffe879f8a2fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435532"
---
# <a name="forms-based-authentication"></a>Проверка подлинности на основе форм

Outlook Social Connector (OSC) вызывает метод [исоЦиалпровидер:: Capabilities](isocialprovider-getcapabilities.md) , который определяет возможности поставщика OSC для социальной сети. Для определения способа поддержки пользователя Office, который выполняет вход в эту социальную сеть, OSC использует возвращенные возможности. 

Если элемент **уселогонвебаус** в возвращенном XML-файле **возможностей** указывает на то, что поставщик OSC поддерживает проверку подлинности на основе форм, OSC может выполнить следующую последовательность вызовов, чтобы разрешить пользователю входить в эту социальную сеть: 
  
1. [ИсоЦиалпровидер:: Load](isocialprovider-load.md) &ndash; OSC загружает поставщика. 
    
2. [ИсоЦиалпровидер:: версия](isocialprovider-version.md) &ndash; OSC возвращает строку, представляющую номер версии поставщика для этой социальной сети. 
    
3. [ИсоЦиалпровидер:: соЦиалнетворкнаме](isocialprovider-socialnetworkname.md) &ndash; OSC возвращает строку, представляющую имя социальной сети. 
    
4. [ИсоЦиалпровидер:: соЦиалнетворкгуид](isocialprovider-socialnetworkguid.md) &ndash; OSC получает неИЗМЕНЯЕМЫЙ идентификатор GUID, представляющий социальную сеть. 
    
5. [ИсоЦиалпровидер:: Capabilities](isocialprovider-getcapabilities.md) &ndash; OSC возвращает строку, представляющую возможности поставщика и которая соответствует определению схемы для элемента **capabilities** . 
    
6. [ИсоЦиалпровидер:: соЦиалнетворкикон](isocialprovider-socialnetworkicon.md) &ndash; OSC возвращает массив байтов, представляющий значок для сайта социальных сетей. 
    
7. [ИсоЦиалпровидер:: @ Session](isocialprovider-getsession.md) &ndash; OSC получает интерфейс [настроенный ISocialSession](isocialsessioniunknown.md) . 
    
8. [Настроенный ISocialSession:: логонвеб](isocialsession-logonweb.md) &ndash; OSC инициализирует вход на сайт социальных сетей с помощью проверки подлинности на основе форм. Для этого первого входного вызова OSC передает **значение NULL** для параметра _Connect_ . 
    
9. [Настроенный ISocialSession:: жетлогонурл](isocialsession-getlogonurl.md) &ndash; OSC получает URL-адрес, который отображает форму на основе браузера для пользователя во время веб-проверки подлинности. 
    
10. [Настроенный ISocialSession:: логонвеб](isocialsession-logonweb.md) &ndash; OSC выполняет вход на сайт социальных сетей с помощью проверки подлинности на основе форм. OSC вызывает этот метод во второй раз, передавая URL-адрес формы входа поставщику в параметре _Connect_ . 
    
11. [Настроенный ISocialSession:: жетлогжедонусер](isocialsession-getloggedonuser.md) &ndash; OSC получает интерфейс [исоЦиалпрофиле](isocialprovideriunknown.md) , представляющий пользователя, выполнившего вход в систему. 
    
12. [Настроенный ISocialSession:: жетнетворкидентифиер](isocialsession-getnetworkidentifier.md) &ndash; OSC возвращает строку, представляющую уникальный идентификатор для сайта социальных сетей. Сетевой идентификатор может быть эквивалентен имени сети. 
    
## <a name="see-also"></a>См. также

- [XML для возможностей](xml-for-capabilities.md)
- [ПереOSC типичные последовательности вызовов](osc-typical-calling-sequences.md)

