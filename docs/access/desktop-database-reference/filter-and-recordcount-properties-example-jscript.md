---
title: Пример использования свойств Filter и RecordCount (JScript)
TOCTitle: Filter and RecordCount properties example (JScript)
ms:assetid: a33e3d13-4184-69f9-4ff2-111106e653cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249755(v=office.15)
ms:contentKeyID: 48546780
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 993209478d18d013771de8239d8e8cd10efc5da2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292491"
---
# <a name="filter-and-recordcount-properties-example-jscript"></a><span data-ttu-id="28795-102">Пример использования свойств Filter и RecordCount (JScript)</span><span class="sxs-lookup"><span data-stu-id="28795-102">Filter and RecordCount properties example (JScript)</span></span>


<span data-ttu-id="28795-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28795-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28795-104">В этом примере открывается объект **Recordset** в таблице "компании" базы данных "Борей", а затем используется свойство [Filter](filter-property-ado.md) , чтобы ограничить отображаемые записи теми записями, в которых поле CompanyName начинается с буквы "D". Скопируйте и вставьте следующий код в блокнот или в другом текстовом редакторе, и сохраните его как **филтержс. ASP**.</span><span class="sxs-lookup"><span data-stu-id="28795-104">This example opens a **Recordset** on the Companies table of the Northwind database and then uses the [Filter](filter-property-ado.md) property to limit the records visible to those where the CompanyName field starts with the letter D. Cut and paste the following code to Notepad or another text editor, and save it as **FilterJS.asp**.</span></span>

