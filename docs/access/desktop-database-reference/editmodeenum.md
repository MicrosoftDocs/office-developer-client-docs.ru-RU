---
title: Едитмодинум (Справочник по базам данных Access на компьютере)
TOCTitle: EditModeEnum
ms:assetid: 4da0e504-aca2-b769-04a2-0df687fa4422
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249248(v=office.15)
ms:contentKeyID: 48544737
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 246d9e29f084efb975783fd15c15993eba5a6e74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293583"
---
# <a name="editmodeenum"></a><span data-ttu-id="3e7dc-102">EditModeEnum</span><span class="sxs-lookup"><span data-stu-id="3e7dc-102">EditModeEnum</span></span>

<span data-ttu-id="3e7dc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e7dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e7dc-104">Задает состояние редактирования записи.</span><span class="sxs-lookup"><span data-stu-id="3e7dc-104">Specifies the editing status of a record.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3e7dc-105">Константа</span><span class="sxs-lookup"><span data-stu-id="3e7dc-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3e7dc-106">Значение</span><span class="sxs-lookup"><span data-stu-id="3e7dc-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3e7dc-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3e7dc-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e7dc-108"><strong>Адедитноне</strong></span><span class="sxs-lookup"><span data-stu-id="3e7dc-108"><strong>adEditNone</strong></span></span></p></td>
<td><p><span data-ttu-id="3e7dc-109">нуль</span><span class="sxs-lookup"><span data-stu-id="3e7dc-109">0</span></span></p></td>
<td><p><span data-ttu-id="3e7dc-110">Указывает, что операции редактирования не выполняются.</span><span class="sxs-lookup"><span data-stu-id="3e7dc-110">Indicates that no editing operation is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e7dc-111"><strong>Адедитинпрогресс</strong></span><span class="sxs-lookup"><span data-stu-id="3e7dc-111"><strong>adEditInProgress</strong></span></span></p></td>
<td><p><span data-ttu-id="3e7dc-112">1,1</span><span class="sxs-lookup"><span data-stu-id="3e7dc-112">1</span></span></p></td>
<td><p><span data-ttu-id="3e7dc-113">Указывает, что данные в текущей записи были изменены, но не были сохранены.</span><span class="sxs-lookup"><span data-stu-id="3e7dc-113">Indicates that data in the current record has been modified but not saved.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e7dc-114"><strong>Адедитадд</strong></span><span class="sxs-lookup"><span data-stu-id="3e7dc-114"><strong>adEditAdd</strong></span></span></p></td>
<td><p><span data-ttu-id="3e7dc-115">2</span><span class="sxs-lookup"><span data-stu-id="3e7dc-115">2</span></span></p></td>
<td><p><span data-ttu-id="3e7dc-116">Указывает на то, что метод <a href="addnew-method-ado.md">AddNew</a> вызван, а текущая запись в буфере копии — это новая запись, которая не была сохранена в базе данных.</span><span class="sxs-lookup"><span data-stu-id="3e7dc-116">Indicates that the <a href="addnew-method-ado.md">AddNew</a> method has been called, and the current record in the copy buffer is a new record that has not been saved in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e7dc-117"><strong>Адедитделете</strong></span><span class="sxs-lookup"><span data-stu-id="3e7dc-117"><strong>adEditDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="3e7dc-118">SP4</span><span class="sxs-lookup"><span data-stu-id="3e7dc-118">4</span></span></p></td>
<td><p><span data-ttu-id="3e7dc-119">Указывает, что текущая запись была удалена.</span><span class="sxs-lookup"><span data-stu-id="3e7dc-119">Indicates that the current record has been deleted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="3e7dc-120">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="3e7dc-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="3e7dc-121">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="3e7dc-121">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3e7dc-122">Константа</span><span class="sxs-lookup"><span data-stu-id="3e7dc-122">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e7dc-123">Адоенумс. EditMode. NONE</span><span class="sxs-lookup"><span data-stu-id="3e7dc-123">AdoEnums.EditMode.NONE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e7dc-124">Адоенумс. EditMode. неВЫПОЛНЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e7dc-124">AdoEnums.EditMode.INPROGRESS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e7dc-125">Адоенумс. EditMode. ADD</span><span class="sxs-lookup"><span data-stu-id="3e7dc-125">AdoEnums.EditMode.ADD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e7dc-126">Адоенумс. EditMode. DELETE</span><span class="sxs-lookup"><span data-stu-id="3e7dc-126">AdoEnums.EditMode.DELETE</span></span></p></td>
</tr>
</tbody>
</table>

