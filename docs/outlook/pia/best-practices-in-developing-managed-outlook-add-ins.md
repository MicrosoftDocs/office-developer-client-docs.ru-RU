---
title: Рекомендации по разработке управляемых надстроек Outlook
TOCTitle: Best practices in developing managed Outlook add-ins
ms:assetid: a03246f6-2ca5-4fcb-8e63-a11cfbc8d9a0
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611563(v=office.15)
ms:contentKeyID: 55119784
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 474a43c17360979b4b25ccb55c0ed48b2c9d2ef7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723098"
---
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a>Рекомендации по разработке управляемых надстроек Outlook

Хотя сборки взаимодействия с Outlook позволяют создавать управляемые решения, которые взаимодействуют с Outlook, эта программа появилась раньше, чем .NET Framework, и разработана с целью поддержки программирования на таких неуправляемых языках, как Visual Basic для приложений (VBA) и Visual Basic. В данном разделе перечислены главные области, о которых нужно иметь представление при разработке управляемой надстройки для Outlook.

- [Систематическое освобождение объектов](systematically-releasing-objects.md)
- [Использование отдельного домена приложений для предотвращения сбоя](using-a-separate-application-domain-to-avoid-crashing.md)
- [Использование надежного объекта приложения, предоставляемого набором "Инструменты разработчика Office для Visual Studio"](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)
- [Правильная установка области применения в обработчиках событий](scoping-variables-appropriately-in-event-handlers.md)
- [Предотвращение использования неподдерживаемых технологий в управляемых надстройках Outlook](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)
- [Использование позднего связывания для нескольких версий Outlook](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)

