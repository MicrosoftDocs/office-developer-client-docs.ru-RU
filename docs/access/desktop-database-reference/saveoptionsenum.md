---
title: SaveOptionsEnum (Справочник по для настольных баз данных Access)
TOCTitle: SaveOptionsEnum
ms:assetid: 2a4e4c7a-6331-7270-0514-cc549c721ffd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249053(v=office.15)
ms:contentKeyID: 48543906
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: ffd37090b264e434b5fd3750f474122f8da4bfbb
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861906"
---
# <a name="saveoptionsenum"></a><span data-ttu-id="2d495-102">SaveOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="2d495-102">SaveOptionsEnum</span></span>

<span data-ttu-id="2d495-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d495-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2d495-104">Указывает, создан или перезаписан при сохранении из объекта [потока](stream-object-ado.md) файла.</span><span class="sxs-lookup"><span data-stu-id="2d495-104">Specifies whether a file should be created or overwritten when saving from a [Stream](stream-object-ado.md) object.</span></span> <span data-ttu-id="2d495-105">Значения может использоваться совместно с оператора AND.</span><span class="sxs-lookup"><span data-stu-id="2d495-105">The values can be combined with an AND operator.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d495-106">Константа</span><span class="sxs-lookup"><span data-stu-id="2d495-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="2d495-107">Значение</span><span class="sxs-lookup"><span data-stu-id="2d495-107">Value</span></span></p></th>
<th><p><span data-ttu-id="2d495-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2d495-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d495-109"><strong>adSaveCreateNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="2d495-109"><strong>adSaveCreateNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="2d495-110">1</span><span class="sxs-lookup"><span data-stu-id="2d495-110">1</span></span></p></td>
<td><p><span data-ttu-id="2d495-111">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d495-111">Default.</span></span> <span data-ttu-id="2d495-112">Создает новый файл, если файл, указанный с помощью параметра <em>имени файла</em> еще не существует.</span><span class="sxs-lookup"><span data-stu-id="2d495-112">Creates a new file if the file specified by the <em>FileName</em> parameter does not already exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d495-113"><strong>adSaveCreateOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="2d495-113"><strong>adSaveCreateOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="2d495-114">2</span><span class="sxs-lookup"><span data-stu-id="2d495-114">2</span></span></p></td>
<td><p><span data-ttu-id="2d495-115">Перезапись файла с данными из открытая в настоящий момент объект <strong>Stream</strong> , если файл, указанный с помощью параметра <em>имени файла</em> уже существует.</span><span class="sxs-lookup"><span data-stu-id="2d495-115">Overwrites the file with the data from the currently open <strong>Stream</strong> object, if the file specified by the <em>Filename</em> parameter already exists.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2d495-116">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2d495-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="2d495-117">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="2d495-117">These constants do not have ADO/WFC equivalents.</span></span>

