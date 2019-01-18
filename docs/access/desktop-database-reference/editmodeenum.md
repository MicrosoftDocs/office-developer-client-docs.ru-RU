---
title: EditModeEnum (Справочник по для настольных баз данных Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 246d9e29f084efb975783fd15c15993eba5a6e74
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726290"
---
# <a name="editmodeenum"></a><span data-ttu-id="2b894-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="2b894-102">EditModeEnum</span></span>

<span data-ttu-id="2b894-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b894-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b894-104">Указывает состояние редактирования записи.</span><span class="sxs-lookup"><span data-stu-id="2b894-104">Specifies the editing status of a record.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b894-105">Константа</span><span class="sxs-lookup"><span data-stu-id="2b894-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="2b894-106">Значение</span><span class="sxs-lookup"><span data-stu-id="2b894-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2b894-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2b894-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b894-108"><strong>как таковые</strong></span><span class="sxs-lookup"><span data-stu-id="2b894-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="2b894-109">0</span><span class="sxs-lookup"><span data-stu-id="2b894-109">0</span></span></p></td>
<td><p><span data-ttu-id="2b894-110">Указывает, что операция редактирования не находится в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="2b894-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b894-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="2b894-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="2b894-112">1</span><span class="sxs-lookup"><span data-stu-id="2b894-112">1</span></span></p></td>
<td><p><span data-ttu-id="2b894-113">Указывает, что данные в текущей записи были изменены, но не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="2b894-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b894-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="2b894-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="2b894-115">2</span><span class="sxs-lookup"><span data-stu-id="2b894-115">2</span></span></p></td>
<td><p><span data-ttu-id="2b894-116">Указывает, что был вызван метод <a href="addnew-method-ado.md">AddNew</a> и текущую запись в буфер копирования является новую запись, которая не была сохранена в базе данных.</span><span class="sxs-lookup"><span data-stu-id="2b894-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b894-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="2b894-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="2b894-118">4</span><span class="sxs-lookup"><span data-stu-id="2b894-118">4</span></span></p></td>
<td><p><span data-ttu-id="2b894-119">Указывает, что текущая запись был удален.</span><span class="sxs-lookup"><span data-stu-id="2b894-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2b894-120">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2b894-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="2b894-121">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="2b894-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b894-122">Константа</span><span class="sxs-lookup"><span data-stu-id="2b894-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b894-123">AdoEnums.EditMode.NONE</span><span class="sxs-lookup"><span data-stu-id="2b894-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b894-124">AdoEnums.EditMode.INPROGRESS</span><span class="sxs-lookup"><span data-stu-id="2b894-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b894-125">AdoEnums.EditMode.ADD</span><span class="sxs-lookup"><span data-stu-id="2b894-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b894-126">AdoEnums.EditMode.DELETE</span><span class="sxs-lookup"><span data-stu-id="2b894-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

