---
title: Размещение InfoPath как редактора XML в другом приложении
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: Среды редактирования форм Microsoft InfoPath могут размещаться в пользовательском приложении Windows позволяет разработчикам интегрировать редактора в бизнес приложениях форм InfoPath.
ms.openlocfilehash: dd87cba7219b5647bd2b20dd67c6eb0f1811cc59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807480"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a><span data-ttu-id="31956-103">Размещение InfoPath как редактора XML в другом приложении</span><span class="sxs-lookup"><span data-stu-id="31956-103">Hosting InfoPath as an XML Editor in Another Application</span></span>

<span data-ttu-id="31956-104">Среды редактирования форм Microsoft InfoPath могут размещаться в пользовательском приложении Windows.</span><span class="sxs-lookup"><span data-stu-id="31956-104">The Microsoft InfoPath form editing environment can be hosted in a custom Windows application.</span></span> <span data-ttu-id="31956-105">Эта функция позволяет разработчикам интегрировать редактора в бизнес приложениях форм InfoPath.</span><span class="sxs-lookup"><span data-stu-id="31956-105">This feature enables developers to integrate the InfoPath form editing environment into line-of-business applications.</span></span> <span data-ttu-id="31956-106">Разработчики традиционных приложений на базе COM можно использовать объект **InfoPathEditorObject** , который доступен с учетом IPEDITOR. DLL-Библиотека, а разработчики Майкрософт. NET-приложений можно использовать сборку **Microsoft.Office.InfoPath.FormControl** , которая предоставляет управляемых типов, на основе интерфейса COM.</span><span class="sxs-lookup"><span data-stu-id="31956-106">Developers writing traditional COM-based applications can use the **InfoPathEditorObject** object that is available by referencing the IPEDITOR.DLL, and developers writing Microsoft .NET-based applications can use the **Microsoft.Office.InfoPath.FormControl** assembly, which provides managed types based on the COM interface.</span></span> <span data-ttu-id="31956-107">IPEDITOR. DLL-Библиотеку и сборки **Microsoft.Office.InfoPath.FormControl** устанавливаются вместе с InfoPath в C:\Program Files\Microsoft Office\Office15 или папка C:\Program Files (x86) \Microsoft Office\Office15.</span><span class="sxs-lookup"><span data-stu-id="31956-107">The IPEDITOR.DLL and **Microsoft.Office.InfoPath.FormControl** assembly are both installed along with InfoPath in the C:\Program Files\Microsoft Office\Office15 or C:\Program Files (x86)\Microsoft Office\Office15 folder.</span></span> 
  
<span data-ttu-id="31956-108">Статья MSDN, размещение среды редактирования форм InfoPath 2007 в пользовательском приложении формы Windows, в центре внимания объект **FormControl** и как включить в пользовательских. NET-приложениях.</span><span class="sxs-lookup"><span data-stu-id="31956-108">The MSDN article, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, focuses on the **FormControl** object and how to incorporate it into your custom .NET-based applications.</span></span> <span data-ttu-id="31956-109">В загружаемом файле, связанным с данной статьей, содержится настраиваемое приложение с функциями технологии .NET по замене среды изменения форм InfoPath за счет использования **IOleCommandTargets** COM.</span><span class="sxs-lookup"><span data-stu-id="31956-109">The download associated with the article contains a custom application that provides .NET functions for replicating the InfoPath form editing environment through the use of COM **IOleCommandTargets**.</span></span>
  

