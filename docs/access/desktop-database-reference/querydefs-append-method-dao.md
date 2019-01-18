---
title: Метод QueryDefs.Append (DAO)
TOCTitle: Append Method
ms:assetid: 9b62a26b-3b7c-6d26-7707-177b00a23178
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198041(v=office.15)
ms:contentKeyID: 48546570
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b4183a7b438d3f55d73eb63adb2d124da7eeecc1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699973"
---
# <a name="querydefsappend-method-dao"></a><span data-ttu-id="fb646-102">Метод QueryDefs.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="fb646-102">QueryDefs.Append method (DAO)</span></span>

<span data-ttu-id="fb646-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb646-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb646-104">Добавляет новый **QueryDef** в коллекцию **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="fb646-104">Adds a new **QueryDef** to the **QueryDefs** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb646-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb646-105">Syntax</span></span>

<span data-ttu-id="fb646-106">*выражение* . Добавление (***объект***)</span><span class="sxs-lookup"><span data-stu-id="fb646-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="fb646-107">*выражение* Переменная, которая представляет собой объект- **QueryDefs** .</span><span class="sxs-lookup"><span data-stu-id="fb646-107">*expression* A variable that represents a **QueryDefs** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb646-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb646-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb646-109">Имя</span><span class="sxs-lookup"><span data-stu-id="fb646-109">Name</span></span></p></th>
<th><p><span data-ttu-id="fb646-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="fb646-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="fb646-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="fb646-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="fb646-112">Описание</span><span class="sxs-lookup"><span data-stu-id="fb646-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb646-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="fb646-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="fb646-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fb646-114">Required</span></span></p></td>
<td><p><span data-ttu-id="fb646-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="fb646-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="fb646-116">Объектная переменная, представляющий поле, добавленный в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="fb646-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fb646-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="fb646-117">Remarks</span></span>

<span data-ttu-id="fb646-118">Добавленный объект становится сохраняемого объекта, хранящиеся на диске, пока не будет удалена с помощью метода **Delete** .</span><span class="sxs-lookup"><span data-stu-id="fb646-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="fb646-119">Добавление нового объекта выполняется немедленно, но следует использовать метод **Refresh** в семействах сайтов, которые может затронуть изменения структуры базы данных.</span><span class="sxs-lookup"><span data-stu-id="fb646-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="fb646-120">Если объект, в которую добавляются не завершена (например, при любые объекты **поля** еще не добавлены в коллекцию **полей** **индекс** объекта до добавляется к коллекции **индексов** ) или задать свойства в одном или нескольких неправильные подчиненных объектов, с помощью метода **Append** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="fb646-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="fb646-121">Например если вы еще не указан тип поля и попытайтесь добавьте объект **поля** в коллекцию **полей** в объекте **TableDef** , с помощью метода **Append** запускает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="fb646-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

