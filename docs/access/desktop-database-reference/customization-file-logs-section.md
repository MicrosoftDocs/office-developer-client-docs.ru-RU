---
title: Customization File Logs Section
TOCTitle: Customization File Logs Section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 479bac0c61718f12af8fcb1b176b91d3fc57841b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482552"
---
# <a name="customization-file-logs-section"></a><span data-ttu-id="3fec8-102">Customization File Logs Section</span><span class="sxs-lookup"><span data-stu-id="3fec8-102">Customization File Logs Section</span></span>

<span data-ttu-id="3fec8-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fec8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3fec8-104">В разделе **Журналы** содержит записи файла журнала, который определяет имя файла, ошибки во время операции **DataFactory**.</span><span class="sxs-lookup"><span data-stu-id="3fec8-104">The **logs** section contains a log file entry, which specifies the name of a file that records errors during the operation of the **DataFactory**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fec8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fec8-105">Syntax</span></span>

<span data-ttu-id="3fec8-106">Запись файла журнала имеет форму:</span><span class="sxs-lookup"><span data-stu-id="3fec8-106">A log file entry is of the form:</span></span>

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3fec8-107">Часть</span><span class="sxs-lookup"><span data-stu-id="3fec8-107">Part</span></span></p></th>
<th><p><span data-ttu-id="3fec8-108">Описание</span><span class="sxs-lookup"><span data-stu-id="3fec8-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fec8-109"><strong>err</strong></span><span class="sxs-lookup"><span data-stu-id="3fec8-109"><strong>err</strong></span></span></p></td>
<td><p><span data-ttu-id="3fec8-110">Строковый литерал, которое указывает, это — это записи файла журнала.</span><span class="sxs-lookup"><span data-stu-id="3fec8-110">A literal string that indicates this is a log file entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fec8-111"><em>Имя файла</em></span><span class="sxs-lookup"><span data-stu-id="3fec8-111"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="3fec8-112">Полный путь и имя файла.</span><span class="sxs-lookup"><span data-stu-id="3fec8-112">A complete path and file name.</span></span> <span data-ttu-id="3fec8-113">Имя файла типичные — <strong>c:\msdfmap.log</strong>.</span><span class="sxs-lookup"><span data-stu-id="3fec8-113">The typical file name is <strong>c:\msdfmap.log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3fec8-114">Файл журнала будет содержать имя пользователя, HRESULT, Дата и время каждой ошибки.</span><span class="sxs-lookup"><span data-stu-id="3fec8-114">The log file will contain the user name, HRESULT, date, and time of each error.</span></span>

