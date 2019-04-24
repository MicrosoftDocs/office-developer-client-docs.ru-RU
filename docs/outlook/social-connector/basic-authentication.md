---
title: Обычная проверка подлинности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89349d1e-365a-442e-9ba3-2df601d9323c
description: 'Outlook Social Connector (OSC) вызывает метод ИсоЦиалпровидер:: capabilities, который определяет возможности поставщика OSC для социальной сети.'
ms.openlocfilehash: 7f716df3ef2e82712374ce3d775cdf66eb07e8b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281223"
---
# <a name="basic-authentication"></a>Обычная проверка подлинности

Outlook Social Connector (OSC) вызывает метод [исоЦиалпровидер:: Capabilities](isocialprovider-getcapabilities.md) , который определяет возможности поставщика OSC для социальной сети. Для определения способа поддержки пользователя Office, который выполняет вход в эту социальную сеть, OSC использует возвращенные возможности. Если элемент **уселогонвебаус** в возвращенном XML-файле **возможностей** указывает, что поставщик OSC поддерживает обычную проверку подлинности, OSC может выполнить следующую последовательность вызовов, чтобы разрешить пользователю входить в эту социальную сеть: 
  
1. [ИсоЦиалпровидер:: Load](isocialprovider-load.md) — элемент OSC загружает поставщик. 
    
2. [ИсоЦиалпровидер:: Version](isocialprovider-version.md) — объект OSC получает строку, представляющую номер версии поставщика OSC. 
    
3. [ИсоЦиалпровидер:: соЦиалнетворкнаме](isocialprovider-socialnetworkname.md) — объект OSC получает строку, представляющую имя социальной сети. 
    
4. [ИсоЦиалпровидер:: соЦиалнетворкгуид](isocialprovider-socialnetworkguid.md) — объект OSC получает неИЗМЕНЯЕМЫЙ идентификатор GUID, представляющий социальную сеть. 
    
5. [ИсоЦиалпровидер::-Capabilities](isocialprovider-getcapabilities.md) — получает строку, представляющую возможности поставщика, и соответствующие определению схемы для элемента **capabilities** . 
    
6. [ИсоЦиалпровидер:: соЦиалнетворкикон](isocialprovider-socialnetworkicon.md) — объект OSC получает массив байтов, представляющий значок для сайта социальных сетей. 
    
7. [ИсоЦиалпровидер::-Session](isocialprovider-getsession.md) — OSC получает интерфейс [настроенный ISocialSession](isocialsessioniunknown.md) . 
    
8. [Настроенный ISocialSession:: вход](isocialsession-logon.md) — OSC выполняет вход пользователя на сайт социальных сетей с использованием указанных имени пользователя и пароля. 
    
9. [Настроенный ISocialSession:: жетлогжедонусер](isocialsession-getloggedonuser.md) — объект OSC получает интерфейс [исоЦиалпрофиле](isocialprovideriunknown.md) , представляющий пользователя, выполнившего вход в систему. 
    
10. [Настроенный ISocialSession:: жетнетворкидентифиер](isocialsession-getnetworkidentifier.md) — объект OSC получает строку, представляющую уникальный идентификатор для сайта социальных сетей. Сетевой идентификатор может быть эквивалентен имени сети. 
    
## <a name="see-also"></a>См. также

- [XML для возможностей](xml-for-capabilities.md)
- [ПереOSC типичные последовательности вызовов](osc-typical-calling-sequences.md)

