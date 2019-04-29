---
title: Получение сведений о друзьях
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: 'Outlook Social Connector (OSC) вызывает метод ИсоЦиалпровидер:: capabilities, который определяет возможности поставщика OSC для социальной сети.'
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428797"
---
# <a name="getting-friends-information"></a>Получение сведений о друзьях

Outlook Social Connector (OSC) вызывает метод [исоЦиалпровидер:: Capabilities](isocialprovider-getcapabilities.md) , который определяет возможности поставщика OSC для социальной сети. Если элементы **** **качефриендс и** в возвращенном XML- **** коде имеют значение, указывающее, что поставщик OSC поддерживает получать и кэшировать друзей как элементы контактов Outlook в соответствующей папке "Контакты", OSC может выполнить Следующая последовательность вызовов. OSC вызывает методы в этой последовательности для получения сведений и изображений (как поддерживается интерфейсом [исоЦиалперсон](isocialpersoniunknown.md) ) для друзей в социальной сети. 
  
> [!NOTE]
> OSC обновляет кэш с интервалом по умолчанию. Если во время обновления кэша возникает ошибка, перемещается на другой заданный интервал, который также можно контролировать, указав элемент **контактсинкрестартинтервал** в XML-коде **возможностей** . Дополнительные сведения об обновлении кэша контактов приведены в статье [Синхронизация друзей и действий](synchronizing-friends-and-activities.md). 
  
1. [Настроенный ISocialSession:: логжедонусерид](isocialsession-loggedonuserid.md) — получает идентификатор пользователя Office, который вошел в социальную сеть. 
    
2. [Настроенный ISocialSession::-Person](isocialsession-getperson.md) — с помощью идентификатора пользователя Office, OSC получает объект **исоЦиалперсон** для этого пользователя. 
    
3. [ИсоЦиалперсон:: жетфриендсандколлеагуес](isocialperson-getfriendsandcolleagues.md) — этот OSC получает список дружественных пользователей в социальной сети. 
    
4. [Настроенный ISocialSession::-Person](isocialsession-getperson.md) — для каждого пользователя в XML-файле, возвращенного **жетфриендсандколлеагуес**, OSC получает интерфейс **исоЦиалперсон** . 
    
5. [ИсоЦиалперсон::](isocialperson-getpicture.md) жетфриендсандколлеагуес — для каждого пользователя в XML-файле, возвращаемого методом ****, OSC получает ресурс изображения.
    
## <a name="see-also"></a>См. также

- [XML для возможностей](xml-for-capabilities.md)
- [ПереOSC типичные последовательности вызовов](osc-typical-calling-sequences.md)

