---
title: Раздел Logs в файле настройки
TOCTitle: Customization File Logs section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a9af5d09a7a7a7a7ec97d757d502efbf2402900
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295151"
---
# <a name="customization-file-logs-section"></a><span data-ttu-id="11325-102">Раздел Logs в файле настройки</span><span class="sxs-lookup"><span data-stu-id="11325-102">Customization File Logs section</span></span>

<span data-ttu-id="11325-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11325-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11325-104">Раздел **logs** содержит запись файла журнала, в которой задается имя файла, записывающего ошибки во время выполнения операции. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="11325-104">The **logs** section contains a log file entry, which specifies the name of a file that records errors during the operation of the **DataFactory**.</span></span>

## <a name="syntax"></a><span data-ttu-id="11325-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11325-105">Syntax</span></span>

<span data-ttu-id="11325-106">Запись файла журнала имеет следующий вид:</span><span class="sxs-lookup"><span data-stu-id="11325-106">A log file entry is of the form:</span></span>

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="11325-107">Часть</span><span class="sxs-lookup"><span data-stu-id="11325-107">Part</span></span></p></th>
<th><p><span data-ttu-id="11325-108">Описание</span><span class="sxs-lookup"><span data-stu-id="11325-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11325-109"><strong>err</strong></span><span class="sxs-lookup"><span data-stu-id="11325-109"><strong>err</strong></span></span></p></td>
<td><p><span data-ttu-id="11325-110">Строка литерала, указывающая на запись в файле журнала.</span><span class="sxs-lookup"><span data-stu-id="11325-110">A literal string that indicates this is a log file entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11325-111"><em>FileName</em></span><span class="sxs-lookup"><span data-stu-id="11325-111"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="11325-112">Полный путь и имя файла.</span><span class="sxs-lookup"><span data-stu-id="11325-112">A complete path and file name.</span></span> <span data-ttu-id="11325-113">Обычное имя файла — <strong>к:\мсдфмап.лог</strong>.</span><span class="sxs-lookup"><span data-stu-id="11325-113">The typical file name is <strong>c:\msdfmap.log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="11325-114">Файл журнала будет содержать имя пользователя, HRESULT, дату и время каждой ошибки.</span><span class="sxs-lookup"><span data-stu-id="11325-114">The log file will contain the user name, HRESULT, date, and time of each error.</span></span>

