---
title: EditModeEnum (Справочник по для настольных баз данных Access)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f2c93f652b76948439cd7f4571608f538155724b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881337"
---
# <a name="editmodeenum"></a><span data-ttu-id="8137c-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="8137c-102">EditModeEnum</span></span>

<span data-ttu-id="8137c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8137c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8137c-104">Указывает состояние редактирования записи.</span><span class="sxs-lookup"><span data-stu-id="8137c-104">Specifies the editing status of a record.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8137c-105">Константа</span><span class="sxs-lookup"><span data-stu-id="8137c-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="8137c-106">Значение</span><span class="sxs-lookup"><span data-stu-id="8137c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8137c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8137c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8137c-108"><strong>как таковые</strong></span><span class="sxs-lookup"><span data-stu-id="8137c-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="8137c-109">0</span><span class="sxs-lookup"><span data-stu-id="8137c-109">0</span></span></p></td>
<td><p><span data-ttu-id="8137c-110">Указывает, что операция редактирования не находится в стадии разработки.</span><span class="sxs-lookup"><span data-stu-id="8137c-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8137c-111"><strong>adEditInProgress</strong></span><span class="sxs-lookup"><span data-stu-id="8137c-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="8137c-112">1</span><span class="sxs-lookup"><span data-stu-id="8137c-112">1</span></span></p></td>
<td><p><span data-ttu-id="8137c-113">Указывает, что данные в текущей записи были изменены, но не сохраняются.</span><span class="sxs-lookup"><span data-stu-id="8137c-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8137c-114"><strong>adEditAdd</strong></span><span class="sxs-lookup"><span data-stu-id="8137c-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="8137c-115">2</span><span class="sxs-lookup"><span data-stu-id="8137c-115">2</span></span></p></td>
<td><p><span data-ttu-id="8137c-116">Указывает, что был вызван метод <a href="addnew-method-ado.md">AddNew</a> и текущую запись в буфер копирования является новую запись, которая не была сохранена в базе данных.</span><span class="sxs-lookup"><span data-stu-id="8137c-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8137c-117"><strong>adEditDelete</strong></span><span class="sxs-lookup"><span data-stu-id="8137c-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="8137c-118">4</span><span class="sxs-lookup"><span data-stu-id="8137c-118">4</span></span></p></td>
<td><p><span data-ttu-id="8137c-119">Указывает, что текущая запись был удален.</span><span class="sxs-lookup"><span data-stu-id="8137c-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8137c-120">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="8137c-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="8137c-121">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="8137c-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8137c-122">Constant</span><span class="sxs-lookup"><span data-stu-id="8137c-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8137c-123">AdoEnums.EditMode.NONE</span><span class="sxs-lookup"><span data-stu-id="8137c-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8137c-124">AdoEnums.EditMode.INPROGRESS</span><span class="sxs-lookup"><span data-stu-id="8137c-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8137c-125">AdoEnums.EditMode.ADD</span><span class="sxs-lookup"><span data-stu-id="8137c-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8137c-126">AdoEnums.EditMode.DELETE</span><span class="sxs-lookup"><span data-stu-id="8137c-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

