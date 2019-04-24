---
title: Метод отношениях. append (DAO)
TOCTitle: Append Method
ms:assetid: dafcc7b8-b30d-2ba2-631d-eca0f882fc2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835334(v=office.15)
ms:contentKeyID: 48548094
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052904
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b8374832ad6cd6bac30fa9d129e54fb6ab4c8fd4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306988"
---
# <a name="relationsappend-method-dao"></a><span data-ttu-id="f9de7-102">Метод отношениях. append (DAO)</span><span class="sxs-lookup"><span data-stu-id="f9de7-102">Relations.Append method (DAO)</span></span>

<span data-ttu-id="f9de7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9de7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9de7-104">Добавляет новое **отношение** в коллекцию **связей** .</span><span class="sxs-lookup"><span data-stu-id="f9de7-104">Adds a new **Relation** to the **Relations** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9de7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9de7-105">Syntax</span></span>

<span data-ttu-id="f9de7-106">*Expression* . Append (***объект***)</span><span class="sxs-lookup"><span data-stu-id="f9de7-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="f9de7-107">*Expression (выражение* ) Переменная, представляющая объект **отношений** .</span><span class="sxs-lookup"><span data-stu-id="f9de7-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9de7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9de7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9de7-109">Имя</span><span class="sxs-lookup"><span data-stu-id="f9de7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f9de7-110">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="f9de7-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="f9de7-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f9de7-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="f9de7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f9de7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9de7-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="f9de7-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="f9de7-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f9de7-114">Required</span></span></p></td>
<td><p><span data-ttu-id="f9de7-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="f9de7-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="f9de7-116">Объектная переменная, представляющая поле, добавляемое в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="f9de7-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f9de7-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="f9de7-117">Remarks</span></span>

<span data-ttu-id="f9de7-118">Добавленный объект становится постоянным объектом, который хранится на диске, пока не будет удален с помощью метода **Delete** .</span><span class="sxs-lookup"><span data-stu-id="f9de7-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="f9de7-119">Добавление нового объекта выполняется немедленно, но необходимо использовать метод **Refresh** для всех остальных коллекций, на которые могут повлиять изменения структуры базы данных.</span><span class="sxs-lookup"><span data-stu-id="f9de7-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="f9de7-120">Если объект, который вы добавляете, не завершен (например, если вы не добавите объекты **field** в коллекцию **Fields** объекта **index** перед добавлением в коллекцию индексов) или \*\*\*\* если свойства задаются в одном или нескольких подчиненные объекты являются неправильными, при использовании метода **append** возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="f9de7-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="f9de7-121">Например, если вы не указали тип поля, а затем пытаетесь добавить объект **field** в коллекцию Fields \*\*\*\* объекта **tabledef** , использование метода **append** вызывает ошибку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="f9de7-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

