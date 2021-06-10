---
title: Коды ошибок ADO
TOCTitle: ADO error codes
ms:assetid: d7cad7f6-9b95-a521-9947-32658f503e3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250086(v=office.15)
ms:contentKeyID: 48548016
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d3d51fa745f17fb07f6a46064ba8ffc626cbb3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283389"
---
# <a name="ado-error-codes"></a><span data-ttu-id="49686-102">Коды ошибок ADO</span><span class="sxs-lookup"><span data-stu-id="49686-102">ADO error codes</span></span>

<span data-ttu-id="49686-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49686-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49686-104">Помимо ошибок поставщика, возвращающихся [](error-object-ado.md) в объектах ошибки из коллекции Ошибок, ADO может возвращать ошибки в механизм обработки исключений среды запуска. [](errors-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="49686-104">In addition to the provider errors returned in the [Error](error-object-ado.md) objects of the [Errors](errors-collection-ado.md) collection, ADO itself can return errors to the exception-handling mechanism of your run-time environment.</span></span> <span data-ttu-id="49686-105">Чтобы зафиксировать ошибки ADO, используйте механизм улавливания ошибок на языке программирования, например заявление on **Error** в Microsoft Visual Basic или блок **try-catch** в Microsoft Visual C++ или Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="49686-105">Use the error trapping mechanism your programming language, such as the **On Error** statement in Microsoft Visual Basic or the **try-catch** block in Microsoft Visual C++ or Microsoft Visual J++ to capture ADO errors.</span></span>

<span data-ttu-id="49686-106">Список кодов ошибок ADO см. в [списке ErrorValueEnum.](errorvalueenum.md)</span><span class="sxs-lookup"><span data-stu-id="49686-106">For the list of ADO error codes, see [ErrorValueEnum](errorvalueenum.md).</span></span>

