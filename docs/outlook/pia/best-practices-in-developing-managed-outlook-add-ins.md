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
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a><span data-ttu-id="5f2b7-102">Рекомендации по разработке управляемых надстроек Outlook</span><span class="sxs-lookup"><span data-stu-id="5f2b7-102">Best practices in developing managed Outlook add-ins</span></span>

<span data-ttu-id="5f2b7-p101">Хотя сборки взаимодействия с Outlook позволяют создавать управляемые решения, которые взаимодействуют с Outlook, эта программа появилась раньше, чем .NET Framework, и разработана с целью поддержки программирования на таких неуправляемых языках, как Visual Basic для приложений (VBA) и Visual Basic. В данном разделе перечислены главные области, о которых нужно иметь представление при разработке управляемой надстройки для Outlook.</span><span class="sxs-lookup"><span data-stu-id="5f2b7-p101">Even though the Outlook interop assemblies allow you to write managed solutions that interoperate with Outlook, Outlook predates the .NET Framework and is designed to support programmability through unmanaged languages such as Visual Basic for Applications (VBA) and Visual Basic. This topic lists the top areas that you should be aware of when you develop a managed add-in for Outlook.</span></span>

- [<span data-ttu-id="5f2b7-105">Систематическое освобождение объектов</span><span class="sxs-lookup"><span data-stu-id="5f2b7-105">Systematically releasing objects</span></span>](systematically-releasing-objects.md)
- [<span data-ttu-id="5f2b7-106">Использование отдельного домена приложений для предотвращения сбоя</span><span class="sxs-lookup"><span data-stu-id="5f2b7-106">Using a separate application domain to avoid crashing</span></span>](using-a-separate-application-domain-to-avoid-crashing.md)
- [<span data-ttu-id="5f2b7-107">Использование надежного объекта приложения, предоставляемого набором "Инструменты разработчика Office для Visual Studio"</span><span class="sxs-lookup"><span data-stu-id="5f2b7-107">Using a trusted application object provided by Office Developer Tools for Visual Studio</span></span>](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)
- [<span data-ttu-id="5f2b7-108">Правильная установка области применения в обработчиках событий</span><span class="sxs-lookup"><span data-stu-id="5f2b7-108">Scoping variables appropriately in event handlers</span></span>](scoping-variables-appropriately-in-event-handlers.md)
- [<span data-ttu-id="5f2b7-109">Предотвращение использования неподдерживаемых технологий в управляемых надстройках Outlook</span><span class="sxs-lookup"><span data-stu-id="5f2b7-109">Avoiding unsupported technologies in managed Outlook add-ins</span></span>](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)
- [<span data-ttu-id="5f2b7-110">Использование позднего связывания для нескольких версий Outlook</span><span class="sxs-lookup"><span data-stu-id="5f2b7-110">Using late binding if depending on multiple versions of Outlook</span></span>](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)

