---
title: Размещение InfoPath как редактора XML в другом приложении
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: Среда редактирования форм Microsoft InfoPath может быть размещена в пользовательском приложении Windows, что позволяет разработчикам интегрировать среду редактирования форм InfoPath в бизнес-приложения.
ms.openlocfilehash: b85e47d506b17982bb883c9d56ea13131807d1cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303691"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a><span data-ttu-id="57b6b-103">Размещение InfoPath как редактора XML в другом приложении</span><span class="sxs-lookup"><span data-stu-id="57b6b-103">Hosting InfoPath as an XML Editor in Another Application</span></span>

<span data-ttu-id="57b6b-104">Среда редактирования форм Microsoft InfoPath может быть размещена в пользовательском приложении Windows.</span><span class="sxs-lookup"><span data-stu-id="57b6b-104">The Microsoft InfoPath form editing environment can be hosted in a custom Windows application.</span></span> <span data-ttu-id="57b6b-105">Эта функция позволяет разработчикам интегрировать среду редактирования форм InfoPath в бизнес-приложения.</span><span class="sxs-lookup"><span data-stu-id="57b6b-105">This feature enables developers to integrate the InfoPath form editing environment into line-of-business applications.</span></span> <span data-ttu-id="57b6b-106">Разработчики традиционных приложений на основе COM могут использовать объект **инфопаседиторобжект** , который можно использовать для создания ссылки на ипедитор. DLL и разработчики, пишущие Майкрософт. NET-приложения могут использовать сборку **Microsoft. Office. InfoPath. формконтрол** , которая предоставляет управляемые типы на основе интерфейса COM.</span><span class="sxs-lookup"><span data-stu-id="57b6b-106">Developers writing traditional COM-based applications can use the **InfoPathEditorObject** object that is available by referencing the IPEDITOR.DLL, and developers writing Microsoft .NET-based applications can use the **Microsoft.Office.InfoPath.FormControl** assembly, which provides managed types based on the COM interface.</span></span> <span data-ttu-id="57b6b-107">ИПЕДИТОР. Сборки DLL и **Microsoft. Office. InfoPath. формконтрол** устанавливаются вместе с InfoPath в папке C:\Program Files\Microsoft Office\Office15 или C:\Program Files (x86) \Microsoft Office\Office15.</span><span class="sxs-lookup"><span data-stu-id="57b6b-107">The IPEDITOR.DLL and **Microsoft.Office.InfoPath.FormControl** assembly are both installed along with InfoPath in the C:\Program Files\Microsoft Office\Office15 or C:\Program Files (x86)\Microsoft Office\Office15 folder.</span></span> 
  
<span data-ttu-id="57b6b-108">Статья MSDN, в которой разМещается среда редактирования форм InfoPath 2007 в пользовательском приложении Windows Form, фокусируется на объекте **формконтрол** и о том, как внедрить его в свой собственный. СЕТЕВЫЕ приложения.</span><span class="sxs-lookup"><span data-stu-id="57b6b-108">The MSDN article, Hosting the InfoPath 2007 Form Editing Environment in a Custom Windows Form Application, focuses on the **FormControl** object and how to incorporate it into your custom .NET-based applications.</span></span> <span data-ttu-id="57b6b-109">В загружаемом файле, связанным с данной статьей, содержится настраиваемое приложение с функциями технологии .NET по замене среды изменения форм InfoPath за счет использования **IOleCommandTargets** COM.</span><span class="sxs-lookup"><span data-stu-id="57b6b-109">The download associated with the article contains a custom application that provides .NET functions for replicating the InfoPath form editing environment through the use of COM **IOleCommandTargets**.</span></span>
  

