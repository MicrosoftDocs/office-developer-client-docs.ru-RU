---
title: Метод Workspaces.Append (DAO)
TOCTitle: Append Method
ms:assetid: 195c26a6-a1d1-40a8-7e7e-13cd632008b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845644(v=office.15)
ms:contentKeyID: 48543498
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11d721d58301d2adb33b2e381d88d7245531ff06
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718887"
---
# <a name="workspacesappend-method-dao"></a><span data-ttu-id="684cc-102">Метод Workspaces.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="684cc-102">Workspaces.Append method (DAO)</span></span>

<span data-ttu-id="684cc-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="684cc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="684cc-104">Добавление новой **рабочей области для** семейства сайтов **рабочих областей** .</span><span class="sxs-lookup"><span data-stu-id="684cc-104">Adds a new **Workspace** to the **Workspaces** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="684cc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="684cc-105">Syntax</span></span>

<span data-ttu-id="684cc-106">*выражение* . Добавление (***объект***)</span><span class="sxs-lookup"><span data-stu-id="684cc-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="684cc-107">*выражение* Переменная, которая представляет собой объект- **рабочие области** .</span><span class="sxs-lookup"><span data-stu-id="684cc-107">*expression* A variable that represents a **Workspaces** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="684cc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="684cc-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="684cc-109">Имя</span><span class="sxs-lookup"><span data-stu-id="684cc-109">Name</span></span></p></th>
<th><p><span data-ttu-id="684cc-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="684cc-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="684cc-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="684cc-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="684cc-112">Описание</span><span class="sxs-lookup"><span data-stu-id="684cc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="684cc-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="684cc-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="684cc-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="684cc-114">Required</span></span></p></td>
<td><p><span data-ttu-id="684cc-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="684cc-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="684cc-116">Объектная переменная, представляющий поле, добавленный в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="684cc-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="684cc-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="684cc-117">Remarks</span></span>

<span data-ttu-id="684cc-118">Добавленный объект становится сохраняемого объекта, хранящиеся на диске, пока не будет удалена с помощью метода **Delete** .</span><span class="sxs-lookup"><span data-stu-id="684cc-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="684cc-119">Добавление нового объекта выполняется немедленно, но следует использовать метод **Refresh** в семействах сайтов, которые может затронуть изменения структуры базы данных.</span><span class="sxs-lookup"><span data-stu-id="684cc-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="684cc-120">Если объект, в которую добавляются не завершена (например, при любые объекты **поля** еще не добавлены в коллекцию **полей** **индекс** объекта до добавляется к коллекции **индексов** ) или задать свойства в одном или нескольких неправильные подчиненных объектов, с помощью метода **Append** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="684cc-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="684cc-121">Например если вы еще не указан тип поля и попытайтесь добавьте объект **поля** в коллекцию **полей** в объекте **TableDef** , с помощью метода **Append** запускает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="684cc-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

