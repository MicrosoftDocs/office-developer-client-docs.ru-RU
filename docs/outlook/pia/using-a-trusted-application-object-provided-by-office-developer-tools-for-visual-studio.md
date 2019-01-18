---
title: Использование надежного объекта Application, предоставляемого инструментами разработчика Office для Visual Studio
TOCTitle: Using a trusted application object provided by Office Developer Tools for Visual Studio
ms:assetid: 3778122f-f60e-48e7-8e72-f3aef168bae2
ms:mtpsurl: https://msdn.microsoft.com/library/Bb622502(v=office.15)
ms:contentKeyID: 55119787
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f86ad294e894b4faea10d033a069638221f1bd78
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703015"
---
# <a name="using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio"></a><span data-ttu-id="edbb9-102">Использование надежного объекта Application, предоставляемого инструментами разработчика Office для Visual Studio</span><span class="sxs-lookup"><span data-stu-id="edbb9-102">Using a trusted Application object provided by Office Developer Tools for Visual Studio</span></span>

<span data-ttu-id="edbb9-103">При разработке управляемой надстройки с помощью инструментов разработчика Office для Visual Studio всегда используйте объект [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)), предоставляемый Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="edbb9-103">If you are developing a managed add-in by using Office Developer Tools for Visual Studio, always use the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object that is provided by Visual Studio.</span></span> 

<span data-ttu-id="edbb9-104">Если вы не планируете автоматизировать новый экземпляр Outlook, не используйте ключевое слово New или new, чтобы создать новый экземпляр Outlook, поскольку защита объектной модели Outlook не считает этот экземпляр объекта **Application** надежным.</span><span class="sxs-lookup"><span data-stu-id="edbb9-104">Unless you intend to automate a new instance of Outlook, do not use the New or new keyword to create a new instance of Outlook, as this instance of the **Application** object is not trusted from the perspective of the Outlook Object Model Guard.</span></span> 

<span data-ttu-id="edbb9-105">Если надстройка использует ненадежные экземпляры объекта **Application**, в зависимости от версии Outlook, работающей в клиенте, надстройка по умолчанию будет вызывать защиту объектной модели Outlook для некоторых элементов объектной модели.</span><span class="sxs-lookup"><span data-stu-id="edbb9-105">If your add-in uses an untrusted instance of the **Application** object, depending on the version of Outlook that the client is running, the add-in by default will invoke Outlook's Object Model Guard on a number of members of the object model.</span></span> 

<span data-ttu-id="edbb9-106">Дополнительные сведения о поведении защиты объектной модели см. в статье [Изменения в Outlook 2007, связанные с безопасностью кода](https://msdn.microsoft.com/library/bb226709\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="edbb9-106">For more information about the behavior of the Object Model Guard, see [Code Security Changes in Outlook 2007](https://msdn.microsoft.com/library/bb226709\(v=office.15\)).</span></span> <span data-ttu-id="edbb9-107">Обратите внимание, что хотя в статье "Изменения в Outlook 2007, связанные с безопасностью кода" надстройки COM считаются надежными по умолчанию, этот дизайн применяется к версиям Outlook, начиная с Outlook 2007, и доверие распространяется на управляемые надстройки аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="edbb9-107">Note that even though the "Code Security Changes in Outlook 2007" article refers to COM add-ins that are trusted by default, this design applies to versions of Outlook since Outlook 2007, and the trust applies to managed add-ins the same way.</span></span> <span data-ttu-id="edbb9-108">Независимо от того, является ли надстройка управляемой или нет, доверие основано на предположении, что надстройка использует надежный объект **Application**.</span><span class="sxs-lookup"><span data-stu-id="edbb9-108">Regardless of whether the add-in is managed or not, the trust is based on the assumption that the add-in uses a trusted **Application** object.</span></span>

