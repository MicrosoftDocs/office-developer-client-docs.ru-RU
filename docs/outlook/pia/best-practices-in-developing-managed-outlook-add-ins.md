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
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a><span data-ttu-id="27924-102">Рекомендации по разработке управляемых надстроек Outlook</span><span class="sxs-lookup"><span data-stu-id="27924-102">Best Practices in Developing Managed Outlook Add-ins</span></span>

<span data-ttu-id="27924-p101">Хотя сборки взаимодействия с Outlook позволяют создавать управляемые решения, которые взаимодействуют с Outlook, эта программа появилась раньше, чем .NET Framework, и разработана с целью поддержки программирования на таких неуправляемых языках, как Visual Basic для приложений (VBA) и Visual Basic. В данном разделе перечислены главные области, о которых нужно иметь представление при разработке управляемой надстройки для Outlook.</span><span class="sxs-lookup"><span data-stu-id="27924-p101">Even though the Outlook interop assemblies allow you to write managed solutions that interoperate with Outlook, Outlook predates the .NET Framework and is designed to support programmability through unmanaged languages such as Visual Basic for Applications (VBA) and Visual Basic. This topic lists the top areas that you should be aware of when you develop a managed add-in for Outlook.</span></span>

- [<span data-ttu-id="27924-105">Систематическое освобождение объектов</span><span class="sxs-lookup"><span data-stu-id="27924-105">Systematically Releasing Objects</span></span>](systematically-releasing-objects.md)
- [<span data-ttu-id="27924-106">Использование отдельного домена приложений для предотвращения сбоя</span><span class="sxs-lookup"><span data-stu-id="27924-106">Using a Separate Application Domain to Avoid Crashing</span></span>](using-a-separate-application-domain-to-avoid-crashing.md)
- [<span data-ttu-id="27924-107">Использование надежного объекта приложения, предоставляемого набором "Инструменты разработчика Office для Visual Studio"</span><span class="sxs-lookup"><span data-stu-id="27924-107">Using a trusted application object provided by Office Developer Tools for Visual Studio</span></span>](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)
- [<span data-ttu-id="27924-108">Правильная установка области применения в обработчиках событий</span><span class="sxs-lookup"><span data-stu-id="27924-108">Scoping Variables Appropriately in Event Handlers</span></span>](scoping-variables-appropriately-in-event-handlers.md)
- [<span data-ttu-id="27924-109">Предотвращение использования неподдерживаемых технологий в управляемых надстройках Outlook</span><span class="sxs-lookup"><span data-stu-id="27924-109">Avoiding Unsupported Technologies in Managed Outlook Add-ins</span></span>](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)
- [<span data-ttu-id="27924-110">Использование позднего связывания для нескольких версий Outlook</span><span class="sxs-lookup"><span data-stu-id="27924-110">Using Late Binding If Depending on Multiple Versions of Outlook</span></span>](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)

