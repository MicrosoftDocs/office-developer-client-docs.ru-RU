---
title: Руководства по программированию в Project 2013
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
f1_keywords:
- error codes
- object model
- Project Server errors
- Project VBA
- PSI
- PSI reference
- VBA
- VBA object model
keywords:
- интерфейс сервера проекта, Project Server, коды ошибок, VBA, Project объектная модель, Project 2013 г., платформа,Visual Basic для приложений, объектная модель Project, объектная модель, Project VBA,Project Server, PSI reference, PSI
localization_priority: Normal
ms.assetid: 79c78c44-1e08-4c9b-a7fe-a5089e666055
description: Найдите обзор ссылки Project Server Interface (PSI), использование интерфейса ASMX и интерфейса WCF PSI, сведения об ошибках Project Server и ссылку на службу OData ProjectData.
ms.openlocfilehash: 27b2eb27d62ec1abdb1a835b5d874e211e7e793e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357038"
---
# <a name="project-2013-programming-references"></a><span data-ttu-id="c562b-104">Руководства по программированию в Project 2013</span><span class="sxs-lookup"><span data-stu-id="c562b-104">Project 2013 programming references</span></span>

<span data-ttu-id="c562b-105">Найдите обзор ссылки Project Server Interface (PSI), способ использования интерфейса ASMX и интерфейса WCF PSI, сведения об ошибках Project Server и ссылку на службу **ProjectData** OData.</span><span class="sxs-lookup"><span data-stu-id="c562b-105">Find an overview of the Project Server Interface (PSI) reference, how to use the ASMX interface and the WCF interface of the PSI, information about Project Server error codes, and a reference for the **ProjectData** OData service.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c562b-106">Основные ссылки на PSI и клиентскую объектную модель (CSOM) в Project Server 2013 см. в следующих [разделах:](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) библиотека классов и ссылка на веб-службы и ссылка на [API JavaScript для Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="c562b-106">For the primary references for the PSI and the client-side object model (CSOM) in Project Server 2013, see the following sections: [Class library and web service reference](https://msdn.microsoft.com/library/ef1830e0-3c9a-4f98-aa0a-5556c298e7d1%28Office.15%29.aspx) and [JavaScript API reference for Project Server 2013](javascript-library-and-rest-reference-for-project-server-2013.md).</span></span> <span data-ttu-id="c562b-107">> Ссылки Office надстройки, которые включают ссылку JavaScript для приложений области задач Project 2013 г., см. в [API JavaScript](https://msdn.microsoft.com/library/fp142185.aspx)для Office .</span><span class="sxs-lookup"><span data-stu-id="c562b-107">> For the Office Add-ins references, which include the JavaScript reference for Project 2013 task pane apps, see [JavaScript API for Office](https://msdn.microsoft.com/library/fp142185.aspx).</span></span> <span data-ttu-id="c562b-108">> Ссылки на VBA за Project стандартный 2013 и Project профессиональный 2013 г. см. в Project [2013 г.](https://msdn.microsoft.com/library/jj235035.aspx)</span><span class="sxs-lookup"><span data-stu-id="c562b-108">> For the VBA reference for Project Standard 2013 and Project Professional 2013, see [Project 2013 VBA developer reference](https://msdn.microsoft.com/library/jj235035.aspx).</span></span> <span data-ttu-id="c562b-109">> ссылки на таблицы отчетов и представления в локальной базе данных Project Server 2013 еще не доступны.</span><span class="sxs-lookup"><span data-stu-id="c562b-109">> The reference for the reporting tables and views in the on-premises Project Server 2013 database is not yet available.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="c562b-110">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="c562b-110">In this section</span></span>

<span data-ttu-id="c562b-111">[Project обзор ссылок PSI](project-psi-reference-overview.md) Описывает сборки и пространства имен в ссылке PSI для Project Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c562b-111">[Project PSI reference overview](project-psi-reference-overview.md) Describes the assemblies and namespaces in the PSI reference for Project Server 2013.</span></span> 
  
<span data-ttu-id="c562b-112">[Необходимые условия для образцов](prerequisites-for-asmx-based-code-samples-in-project.md) кода на основе ASMX в Project Описывает, как использовать образцы кода в ссылке PSI, которая строится с помощью веб-служб ASMX в тестовых приложениях.</span><span class="sxs-lookup"><span data-stu-id="c562b-112">[Prerequisites for ASMX-based code samples in Project](prerequisites-for-asmx-based-code-samples-in-project.md) Describes how to use code samples in the PSI reference that are built by using ASMX web services in your test applications.</span></span> 
  
<span data-ttu-id="c562b-113">Необходимые условия для образцов кода на основе [WCF в Project](prerequisites-for-wcf-based-code-samples-in-project.md) Описывает использование образцов кода в ссылке PSI, которая строится с помощью служб Windows Communication Foundation (WCF) в тестовых приложениях.</span><span class="sxs-lookup"><span data-stu-id="c562b-113">[Prerequisites for WCF-based code samples in Project](prerequisites-for-wcf-based-code-samples-in-project.md) Describes how to use code samples in the PSI reference that are built by using Windows Communication Foundation (WCF) services in your test applications.</span></span> 
  
<span data-ttu-id="c562b-114">[Project коды ошибок сервера](project-server-error-codes.md) Списки кодов и описаний ошибок Project Server по функциональной области.</span><span class="sxs-lookup"><span data-stu-id="c562b-114">[Project Server error codes](project-server-error-codes.md) Lists the codes and descriptions of Project Server errors by functional area.</span></span> 
  
<span data-ttu-id="c562b-115">[ProjectData — Project ссылки на службу OData](https://msdn.microsoft.com/library/office/jj163015.aspx) Включает обзор службы OData для данных отчетов Project Server, введение в использование каналов OData с запросами LINQ и ссылки на метаданные XML в службе **ProjectData.**</span><span class="sxs-lookup"><span data-stu-id="c562b-115">[ProjectData - Project OData service reference](https://msdn.microsoft.com/library/office/jj163015.aspx) Includes an overview of the OData service for Project Server reporting data, an introduction to using the OData feeds with LINQ queries, and references for the XML metadata in the **ProjectData** service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c562b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="c562b-116">See also</span></span>



[<span data-ttu-id="c562b-117">API JavaScript для Office</span><span class="sxs-lookup"><span data-stu-id="c562b-117">JavaScript API for Office</span></span>](https://msdn.microsoft.com/library/fp142185.aspx)
  
[<span data-ttu-id="c562b-118">Project 2013 ссылка на разработчика VBA</span><span class="sxs-lookup"><span data-stu-id="c562b-118">Project 2013 VBA developer reference</span></span>](https://msdn.microsoft.com/library/jj235035.aspx)

