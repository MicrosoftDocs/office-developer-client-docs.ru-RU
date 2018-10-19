---
title: Рекомендации по разработке управляемых надстроек Outlook
TOCTitle: Best practices in developing managed Outlook add-ins
ms:assetid: a03246f6-2ca5-4fcb-8e63-a11cfbc8d9a0
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611563(v=office.15)
ms:contentKeyID: 55119784
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 87573980836d63d751302b0efcec0952331b7fc4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406864"
---
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a>Рекомендации по разработке управляемых надстроек Outlook

Хотя сборки взаимодействия с Outlook позволяют создавать управляемые решения, которые взаимодействуют с Outlook, эта программа появилась раньше, чем .NET Framework, и разработана с целью поддержки программирования на таких неуправляемых языках, как Visual Basic для приложений (VBA) и Visual Basic. В данном разделе перечислены главные области, о которых нужно иметь представление при разработке управляемой надстройки для Outlook.

- [Систематическое освобождение объектов](systematically-releasing-objects.md)
- [Использование отдельного домена приложений для предотвращения сбоя](using-a-separate-application-domain-to-avoid-crashing.md)
- [Использование надежного объекта приложения, предоставляемого набором "Инструменты разработчика Office для Visual Studio"](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)
- [Правильная установка области применения в обработчиках событий](scoping-variables-appropriately-in-event-handlers.md)
- [Предотвращение использования неподдерживаемых технологий в управляемых надстройках Outlook](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)
- [Использование позднего связывания для нескольких версий Outlook](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)

