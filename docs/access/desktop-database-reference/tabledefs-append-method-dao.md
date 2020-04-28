---
title: Методы TableDef. append (DAO)
TOCTitle: Append Method
ms:assetid: f951a3c4-dade-c1ef-3bfc-6b2a60e12adc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837001(v=office.15)
ms:contentKeyID: 48548811
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 31eca3f4ca5993a401bd85a4b04299a8697c16e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314380"
---
# <a name="tabledefsappend-method-dao"></a><span data-ttu-id="3b500-102">Методы TableDef. append (DAO)</span><span class="sxs-lookup"><span data-stu-id="3b500-102">TableDefs.Append method (DAO)</span></span>

<span data-ttu-id="3b500-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b500-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b500-104">Добавляет новый объект **tabledef** в коллекцию **tabledef** .</span><span class="sxs-lookup"><span data-stu-id="3b500-104">Adds a new **TableDef** to the **TableDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b500-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b500-105">Syntax</span></span>

<span data-ttu-id="3b500-106">*выражение* .Append(***Object***)</span><span class="sxs-lookup"><span data-stu-id="3b500-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="3b500-107">*Expression (выражение* ) Переменная, представляющая объект **TableDefs** .</span><span class="sxs-lookup"><span data-stu-id="3b500-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b500-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b500-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b500-109">Имя</span><span class="sxs-lookup"><span data-stu-id="3b500-109">Name</span></span></p></th>
<th><p><span data-ttu-id="3b500-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="3b500-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="3b500-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3b500-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="3b500-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3b500-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b500-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="3b500-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="3b500-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3b500-114">Required</span></span></p></td>
<td><p><span data-ttu-id="3b500-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="3b500-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="3b500-116">Объектная переменная, представляющая поле, которое добавляется в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="3b500-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3b500-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="3b500-117">Remarks</span></span>

<span data-ttu-id="3b500-118">Добавляемый объект становится постоянным объектом, хранящимся на диске, пока вы не удалите его с помощью метода **Delete**.</span><span class="sxs-lookup"><span data-stu-id="3b500-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="3b500-119">Добавление нового объекта происходит незамедлительно, но следует применить метод **Refresh** для любых других коллекций, которые могут быть затронуты изменениями в структуре базы данных.</span><span class="sxs-lookup"><span data-stu-id="3b500-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="3b500-120">Если добавляемый объект неполный (например, если не добавлены объекты **Field** в коллекцию **Fields** объекта **Index** перед его добавлением в коллекцию **Indexes**) или заданы неверные свойства в одном или нескольких подчиненных объектах, применение метода **Append** вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="3b500-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="3b500-121">Например, если не указан тип поля и выполняется попытка добавить объект **Field** в коллекцию **Fields** объекта **TableDef**, применение метода **Append** вызывает ошибку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="3b500-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

