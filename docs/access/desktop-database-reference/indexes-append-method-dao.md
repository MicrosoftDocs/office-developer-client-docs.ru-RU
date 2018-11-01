---
title: Indexes.Append Method (DAO)
TOCTitle: Append Method
ms:assetid: 60dce80f-505b-e988-3ac1-8ecaae3d3d09
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194835(v=office.15)
ms:contentKeyID: 48545191
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 203be6662fe555ecac0d6d18b261c6d5409700e3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873910"
---
# <a name="indexesappend-method-dao"></a><span data-ttu-id="0e4a2-102">Indexes.Append Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="0e4a2-102">Indexes.Append Method (DAO)</span></span>


<span data-ttu-id="0e4a2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e4a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e4a2-104">Добавляет новый **индекс** коллекции **индексов** .</span><span class="sxs-lookup"><span data-stu-id="0e4a2-104">Adds a new **Index** to the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e4a2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e4a2-105">Syntax</span></span>

<span data-ttu-id="0e4a2-106">*выражение* . Добавление (***объект***)</span><span class="sxs-lookup"><span data-stu-id="0e4a2-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="0e4a2-107">*выражение* Переменная, которая представляет объект **индексов** .</span><span class="sxs-lookup"><span data-stu-id="0e4a2-107">*expression* A variable that represents an **Indexes** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="0e4a2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e4a2-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e4a2-109">Имя</span><span class="sxs-lookup"><span data-stu-id="0e4a2-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0e4a2-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="0e4a2-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0e4a2-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0e4a2-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="0e4a2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0e4a2-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e4a2-113">Объект</span><span class="sxs-lookup"><span data-stu-id="0e4a2-113">Object</span></span></p></td>
<td><p><span data-ttu-id="0e4a2-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0e4a2-114">Required</span></span></p></td>
<td><p><span data-ttu-id="0e4a2-115"><strong>Объект</strong></span><span class="sxs-lookup"><span data-stu-id="0e4a2-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="0e4a2-116">Объектная переменная, который представляет элемент, добавленный в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="0e4a2-116">An object variable that represents the item being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0e4a2-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="0e4a2-117">Remarks</span></span>

<span data-ttu-id="0e4a2-118">Добавленный объект становится сохраняемого объекта, хранящиеся на диске, пока не будет удалена с помощью метода **Delete** .</span><span class="sxs-lookup"><span data-stu-id="0e4a2-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="0e4a2-119">Добавление нового объекта выполняется немедленно, но следует использовать метод **Refresh** в семействах сайтов, которые может затронуть изменения структуры базы данных.</span><span class="sxs-lookup"><span data-stu-id="0e4a2-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="0e4a2-120">Если объект, в которую добавляются не завершена (например, при любые объекты **поля** еще не добавлены в коллекцию **полей** **индекс** объекта до добавляется к коллекции **индексов** ) или задать свойства в одном или нескольких неправильные подчиненных объектов, с помощью метода **Append** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="0e4a2-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="0e4a2-121">Например если вы еще не указан тип поля и попытайтесь добавьте объект **поля** в коллекцию **полей** в объекте **TableDef** , с помощью метода **Append** запускает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="0e4a2-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

