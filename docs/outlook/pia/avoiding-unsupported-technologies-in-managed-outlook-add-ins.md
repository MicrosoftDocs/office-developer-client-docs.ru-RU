---
title: Предотвращение использования неподдерживаемых технологий в управляемых надстройках Outlook
TOCTitle: Avoiding unsupported technologies in managed Outlook add-ins
ms:assetid: 365fd319-725f-4c4b-b6e7-575f78ed8bda
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb610014(v=office.15)
ms:contentKeyID: 55119789
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 99cdfc2447e6bf63078eb87bb9546d8b07ee83e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359061"
---
# <a name="avoiding-unsupported-technologies-in-managed-outlook-add-ins"></a><span data-ttu-id="69023-102">Предотвращение использования неподдерживаемых технологий в управляемых надстройках Outlook</span><span class="sxs-lookup"><span data-stu-id="69023-102">Avoiding unsupported technologies in managed Outlook add-ins</span></span>

<span data-ttu-id="69023-103">Некоторые технологии, применявшиеся до .NET Framework, не поддерживаются в управляемом программном коде.</span><span class="sxs-lookup"><span data-stu-id="69023-103">Certain technologies that predate the .NET Framework are not supported in managed code programming.</span></span> <span data-ttu-id="69023-104">Эти технологии включают объекты данных совместной работы (CDO), интерфейс MAPI (часто называемый расширенным MAPI) и Simple MAPI.</span><span class="sxs-lookup"><span data-stu-id="69023-104">These technologies include Collaboration Data Objects (CDO), Messaging Application Programming Interface (MAPI, often known as Extended MAPI), and Simple MAPI.</span></span> <span data-ttu-id="69023-105">Эти технологии были разработаны с помощью неуправляемого кода, и корпорация Майкрософт не предоставляет официальных управляемых оболочек для поддержки их использования в управляемых приложениях.</span><span class="sxs-lookup"><span data-stu-id="69023-105">These technologies were designed and developed with unmanaged code, and Microsoft does not provide official managed wrappers to support their use in managed applications.</span></span> 

<span data-ttu-id="69023-106">Дополнительные сведения см. в разделе "API, которые поддерживаются в управляемом коде" статьи базы знаний [KB 266353: рекомендации поддержки для разработки клиентской системы обмена сообщениями](https://go.microsoft.com/fwlink/?linkid=89209).</span><span class="sxs-lookup"><span data-stu-id="69023-106">For more information, see the section "APIs that are supported in managed code" in the article [KB 266353: The support guidelines for client-side messaging development](https://go.microsoft.com/fwlink/?linkid=89209).</span></span>

<span data-ttu-id="69023-107">Тем не менее, Microsoft Outlook предлагает множество компонентов объектной модели, выполняющих те же функции, которые ранее были доступны для разработчиков только в CDO или клиентских расширениях Exchange (ECE).</span><span class="sxs-lookup"><span data-stu-id="69023-107">Nonetheless, Microsoft Outlook offers many object model features that achieve what previously only CDO and Exchange Client Extensions (ECE) solved for developers.</span></span> <span data-ttu-id="69023-108">Если вы используете CDO в существующем неуправляемом приложении Outlook и отсутствие поддержки для CDO в управляемых решениях затрудняло миграцию приложения в управляемый код, то теперь можно предусмотреть обновление решения до управляемого кода с использованием только объектной модели Outlook и основной сборки взаимодействия (PIA), не прибегая к CDO.</span><span class="sxs-lookup"><span data-stu-id="69023-108">If you use CDO in an existing unmanaged Outlook application and the lack of support for CDO in managed solutions has hindered you from migrating the application to managed code, you can now consider updating your solution to managed code, using only the Outlook object model and the Primary Interop Assembly (PIA), without having to resort to CDO.</span></span> 

<span data-ttu-id="69023-109">Дополнительные сведения о более универсальной платформе Outlook, внедренной в Outlook 2007 для уменьшения зависимости от CDO и ECE, см. в статье [Новые возможности для разработчиков в Outlook 2007 (часть 1 из 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="69023-109">For more information about a more comprehensive Outlook platform introduced in Outlook 2007 to reduce reliance on CDO and ECE, see [What's New for Developers in Outlook 2007 (Part 1 of 2)](https://msdn.microsoft.com/library/bb226711\(v=office.15\)).</span></span>

