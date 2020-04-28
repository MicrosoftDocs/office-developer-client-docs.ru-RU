---
title: Метод workspaces. append (DAO)
TOCTitle: Append Method
ms:assetid: 195c26a6-a1d1-40a8-7e7e-13cd632008b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845644(v=office.15)
ms:contentKeyID: 48543498
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11d721d58301d2adb33b2e381d88d7245531ff06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302494"
---
# <a name="workspacesappend-method-dao"></a><span data-ttu-id="572bc-102">Метод workspaces. append (DAO)</span><span class="sxs-lookup"><span data-stu-id="572bc-102">Workspaces.Append method (DAO)</span></span>

<span data-ttu-id="572bc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="572bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="572bc-104">Добавляет новую **рабочую область** в коллекцию **workspaces** .</span><span class="sxs-lookup"><span data-stu-id="572bc-104">Adds a new **Workspace** to the **Workspaces** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="572bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="572bc-105">Syntax</span></span>

<span data-ttu-id="572bc-106">*выражение* .Append(***Object***)</span><span class="sxs-lookup"><span data-stu-id="572bc-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="572bc-107">*Expression (выражение* ) Переменная, представляющая объект **workspaces** .</span><span class="sxs-lookup"><span data-stu-id="572bc-107">*expression* A variable that represents a **Workspaces** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="572bc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="572bc-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="572bc-109">Имя</span><span class="sxs-lookup"><span data-stu-id="572bc-109">Name</span></span></p></th>
<th><p><span data-ttu-id="572bc-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="572bc-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="572bc-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="572bc-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="572bc-112">Описание</span><span class="sxs-lookup"><span data-stu-id="572bc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="572bc-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="572bc-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="572bc-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="572bc-114">Required</span></span></p></td>
<td><p><span data-ttu-id="572bc-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="572bc-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="572bc-116">Объектная переменная, представляющая поле, которое добавляется в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="572bc-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="572bc-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="572bc-117">Remarks</span></span>

<span data-ttu-id="572bc-118">Добавляемый объект становится постоянным объектом, хранящимся на диске, пока вы не удалите его с помощью метода **Delete**.</span><span class="sxs-lookup"><span data-stu-id="572bc-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="572bc-119">Добавление нового объекта происходит незамедлительно, но следует применить метод **Refresh** для любых других коллекций, которые могут быть затронуты изменениями в структуре базы данных.</span><span class="sxs-lookup"><span data-stu-id="572bc-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="572bc-120">Если добавляемый объект неполный (например, если не добавлены объекты **Field** в коллекцию **Fields** объекта **Index** перед его добавлением в коллекцию **Indexes**) или заданы неверные свойства в одном или нескольких подчиненных объектах, применение метода **Append** вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="572bc-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="572bc-121">Например, если не указан тип поля и выполняется попытка добавить объект **Field** в коллекцию **Fields** объекта **TableDef**, применение метода **Append** вызывает ошибку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="572bc-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

