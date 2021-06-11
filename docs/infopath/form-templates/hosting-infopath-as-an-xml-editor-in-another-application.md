---
title: Размещение InfoPath как редактора XML в другом приложении
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: Среда редактирования форм Microsoft InfoPath может быть организована в настраиваемом приложении Windows, которое позволяет разработчикам интегрировать среду редактирования форм InfoPath в бизнес-приложения.
ms.openlocfilehash: b85e47d506b17982bb883c9d56ea13131807d1cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422581"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a><span data-ttu-id="b7cfc-103">Размещение InfoPath как редактора XML в другом приложении</span><span class="sxs-lookup"><span data-stu-id="b7cfc-103">Hosting InfoPath as an XML Editor in Another Application</span></span>

<span data-ttu-id="b7cfc-104">Среда редактирования форм Microsoft InfoPath может быть организована в настраиваемом Windows приложении.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-104">The Microsoft InfoPath form editing environment can be hosted in a custom Windows application.</span></span> <span data-ttu-id="b7cfc-105">Эта функция позволяет разработчикам интегрировать среду редактирования форм InfoPath в бизнес-приложения.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-105">This feature enables developers to integrate the InfoPath form editing environment into line-of-business applications.</span></span> <span data-ttu-id="b7cfc-106">Разработчики, пишующие традиционные com-приложения, могут использовать объект **InfoPathEditorObject,** доступный, ссылаясь на IPEDITOR.DLL, и разработчики, пишующие Microsoft . Приложения на основе NET могут использовать **Microsoft.Office. Сборка InfoPath.FormControl,** которая предоставляет управляемые типы на основе интерфейса COM.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-106">Developers writing traditional COM-based applications can use the **InfoPathEditorObject** object that is available by referencing the IPEDITOR.DLL, and developers writing Microsoft .NET-based applications can use the **Microsoft.Office.InfoPath.FormControl** assembly, which provides managed types based on the COM interface.</span></span> <span data-ttu-id="b7cfc-107">В IPEDITOR.DLL **Microsoft.Office. Сборка InfoPath.FormControl** устанавливается вместе с InfoPath в папке C:\Program Files\Microsoft Office\Office15 или C:\Program Files (x86)\Microsoft Office\Office15.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-107">The IPEDITOR.DLL and **Microsoft.Office.InfoPath.FormControl** assembly are both installed along with InfoPath in the C:\Program Files\Microsoft Office\Office15 or C:\Program Files (x86)\Microsoft Office\Office15 folder.</span></span> 
  
<span data-ttu-id="b7cfc-108">В статье MSDN, размещенной в среде редактирования форм InfoPath 2007 в настраиваемом приложении Windows формы, основное внимание уделяется объекту **FormControl** и его включению в настраиваемый . NET-приложения.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-108">The MSDN article, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, focuses on the **FormControl** object and how to incorporate it into your custom .NET-based applications.</span></span> <span data-ttu-id="b7cfc-109">В загружаемом файле, связанным с данной статьей, содержится настраиваемое приложение с функциями технологии .NET по замене среды изменения форм InfoPath за счет использования **IOleCommandTargets** COM.</span><span class="sxs-lookup"><span data-stu-id="b7cfc-109">The download associated with the article contains a custom application that provides .NET functions for replicating the InfoPath form editing environment through the use of COM **IOleCommandTargets**.</span></span>
  

