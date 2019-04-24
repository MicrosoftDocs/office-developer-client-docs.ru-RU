---
title: Ошибки (Справочник по базам данных Access на компьютере)
TOCTitle: Errors
ms:assetid: 42f5cab9-f32a-d789-10e8-8d73892427f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249199(v=office.15)
ms:contentKeyID: 48544490
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 056ec0b34991348728898b4c0fc4a1a516a9913f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293359"
---
# <a name="errors"></a><span data-ttu-id="cddaf-102">Ошибки</span><span class="sxs-lookup"><span data-stu-id="cddaf-102">Errors</span></span>

<span data-ttu-id="cddaf-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cddaf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cddaf-104">Любая операция, включающая объекты ADO, может создавать одну или несколько ошибок поставщика.</span><span class="sxs-lookup"><span data-stu-id="cddaf-104">Any operation involving ADO objects can generate one or more provider errors.</span></span> <span data-ttu-id="cddaf-105">При возникновении каждой ошибки в коллекцию Errors объекта **Connection** помещаются один \*\*\*\* или несколько объектов **Error** .</span><span class="sxs-lookup"><span data-stu-id="cddaf-105">As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object.</span></span> <span data-ttu-id="cddaf-106">Подробные сведения об обработке предупреждений и ошибок в приложении ADO содержатся в [главе 6: обработка ошибок](chapter-6-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="cddaf-106">For details about handling warnings and errors in your ADO application, see [Chapter 6: Error handling](chapter-6-error-handling.md).</span></span>

<span data-ttu-id="cddaf-107">Ошибки приложений могут быть вызваны отдельным механизмом.</span><span class="sxs-lookup"><span data-stu-id="cddaf-107">Application errors can be raised by a separate mechanism.</span></span> <span data-ttu-id="cddaf-108">Например, в Visual Basic объект **Err** будет содержать ошибки на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="cddaf-108">For example, in Visual Basic, the **Err** object will contain application-level errors.</span></span>

