---
title: Метод Properties.Append (DAO)
TOCTitle: Append Method
ms:assetid: 47f1e24f-975c-3fdc-5c3c-8c91f2920c81
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193232(v=office.15)
ms:contentKeyID: 48544609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 528809495ebefd15a8895b15a9d51f84e6892980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301311"
---
# <a name="propertiesappend-method-dao"></a><span data-ttu-id="228b8-102">Метод Properties.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="228b8-102">Properties.Append method (DAO)</span></span>

<span data-ttu-id="228b8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="228b8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="228b8-104">Добавляет новое **свойство** в коллекцию **Свойств.**</span><span class="sxs-lookup"><span data-stu-id="228b8-104">Adds a new **Property** to the **Properties** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="228b8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="228b8-105">Syntax</span></span>

<span data-ttu-id="228b8-106">*выражение* .Append(***Object***)</span><span class="sxs-lookup"><span data-stu-id="228b8-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="228b8-107">*выражение* Переменная, представляюная объект **Properties.**</span><span class="sxs-lookup"><span data-stu-id="228b8-107">*expression* A variable that represents a **Properties** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="228b8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="228b8-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="228b8-109">Имя</span><span class="sxs-lookup"><span data-stu-id="228b8-109">Name</span></span></p></th>
<th><p><span data-ttu-id="228b8-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="228b8-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="228b8-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="228b8-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="228b8-112">Описание</span><span class="sxs-lookup"><span data-stu-id="228b8-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="228b8-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="228b8-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="228b8-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="228b8-114">Required</span></span></p></td>
<td><p><span data-ttu-id="228b8-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="228b8-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="228b8-116">Объектная переменная, представляющая поле, которое добавляется в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="228b8-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="228b8-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="228b8-117">Remarks</span></span>

<span data-ttu-id="228b8-118">Добавляемый объект становится постоянным объектом, хранящимся на диске, пока вы не удалите его с помощью метода **Delete**.</span><span class="sxs-lookup"><span data-stu-id="228b8-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="228b8-119">Добавление нового объекта происходит незамедлительно, но следует применить метод **Refresh** для любых других коллекций, которые могут быть затронуты изменениями в структуре базы данных.</span><span class="sxs-lookup"><span data-stu-id="228b8-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="228b8-120">Если добавляемый объект неполный (например, если не добавлены объекты **Field** в коллекцию **Fields** объекта **Index** перед его добавлением в коллекцию **Indexes**) или заданы неверные свойства в одном или нескольких подчиненных объектах, применение метода **Append** вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="228b8-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="228b8-121">Например, если не указан тип поля и выполняется попытка добавить объект **Field** в коллекцию **Fields** объекта **TableDef**, применение метода **Append** вызывает ошибку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="228b8-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

