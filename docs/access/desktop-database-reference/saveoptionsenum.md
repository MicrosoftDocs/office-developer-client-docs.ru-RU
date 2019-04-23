---
title: Савеоптионсенум (Справочник по базам данных Access на компьютере)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77a617dc54d8acd145648d926e10cf7c9a3cf252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314744"
---
# <a name="saveoptionsenum"></a><span data-ttu-id="9e7a8-102">SaveOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="9e7a8-102">SaveOptionsEnum</span></span>

<span data-ttu-id="9e7a8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e7a8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e7a8-104">Указывает, следует ли создать или перезаписать файл при сохранении из объекта [Stream](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="9e7a8-104">Specifies whether a file should be created or overwritten when saving from a [Stream](stream-object-ado.md) object.</span></span> <span data-ttu-id="9e7a8-105">Значения можно сочетать с помощью оператора AND.</span><span class="sxs-lookup"><span data-stu-id="9e7a8-105">The values can be combined with an AND operator.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e7a8-106">Константа</span><span class="sxs-lookup"><span data-stu-id="9e7a8-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="9e7a8-107">Значение</span><span class="sxs-lookup"><span data-stu-id="9e7a8-107">Value</span></span></p></th>
<th><p><span data-ttu-id="9e7a8-108">Описание</span><span class="sxs-lookup"><span data-stu-id="9e7a8-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e7a8-109"><strong>Адсавекреатенотексист</strong></span><span class="sxs-lookup"><span data-stu-id="9e7a8-109"><strong>adSaveCreateNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="9e7a8-110">1,1</span><span class="sxs-lookup"><span data-stu-id="9e7a8-110">1</span></span></p></td>
<td><p><span data-ttu-id="9e7a8-111">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9e7a8-111">Default.</span></span> <span data-ttu-id="9e7a8-112">Создает новый файл, если файл, указанный с помощью параметра <em>filename</em> , еще не существует.</span><span class="sxs-lookup"><span data-stu-id="9e7a8-112">Creates a new file if the file specified by the <em>FileName</em> parameter does not already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e7a8-113"><strong>Адсавекреатеоверврите</strong></span><span class="sxs-lookup"><span data-stu-id="9e7a8-113"><strong>adSaveCreateOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="9e7a8-114">2</span><span class="sxs-lookup"><span data-stu-id="9e7a8-114">2</span></span></p></td>
<td><p><span data-ttu-id="9e7a8-115">Перезаписывает файл данными из текущего открытого объекта <strong>Stream</strong> , если файл, указанный с помощью параметра <em>filename</em> , уже существует.</span><span class="sxs-lookup"><span data-stu-id="9e7a8-115">Overwrites the file with the data from the currently open <strong>Stream</strong> object, if the file specified by the <em>Filename</em> parameter already exists.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="9e7a8-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="9e7a8-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="9e7a8-117">Эти константы не имеют эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="9e7a8-117">These constants do not have ADO/WFC equivalents.</span></span>

